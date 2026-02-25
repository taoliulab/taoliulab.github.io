---
layout: post
title: "Tutorial: Snakemake quickstart"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short, practical guide for new lab members running **Snakemake on UB CCR** (SLURM usage only).

Official references:
- Snakemake CLI docs: <https://snakemake.readthedocs.io/en/stable/executing/cli.html>
- Snakemake SLURM executor plugin: <https://snakemake.github.io/snakemake-plugin-catalog/plugins/executor/slurm.html>
- CCR jobs docs: <https://docs.ccr.buffalo.edu/en/latest/hpc/jobs/>

## 1) Login and prepare environment

```bash
ssh <CCRUsername>@vortex.ccr.buffalo.edu
module load gcc python
python3 -m venv /projects/academic/<YourGroupName>/venvs/snakemake
source /projects/academic/<YourGroupName>/venvs/snakemake/bin/activate
pip install --upgrade pip
pip install snakemake snakemake-executor-plugin-slurm
```

## 2) Create minimal workflow files

Create `Snakefile`:

```python
rule all:
    input:
        "results/hello.txt"

rule hello:
    output:
        "results/hello.txt"
    shell:
        "mkdir -p results && echo hello_ccr > {output}"
```

## 3) Dry run first (always)

```bash
snakemake -n --cores 1
```

## 4) Run on CCR with SLURM executor

```bash
snakemake \
  --executor slurm \
  --jobs 50 \
  --default-resources mem_mb=4000 runtime=60 \
  --set-resources hello:slurm_account=<SlurmAccountName> \
  --set-resources hello:slurm_partition=general-compute
```

Notes:
- Use your real account/partition values from `slimits`.
- Keep resource requests realistic to avoid long queue wait.

## 5) Recommended profile (cleaner for lab usage)

Create `profiles/ccr/config.v8+.yaml`:

```yaml
executor: slurm
jobs: 100
default-resources:
  mem_mb: 4000
  runtime: 60
set-resources:
  hello:
    slurm_account: <SlurmAccountName>
    slurm_partition: general-compute
```

Run with:

```bash
snakemake --profile profiles/ccr -n
snakemake --profile profiles/ccr
```

## 6) Monitor and troubleshoot

```bash
squeue -u $USER
sacct -j <jobid> --format=JobID,State,Elapsed,ReqMem,MaxRSS
```

Common issues:
- Missing/invalid Slurm account → check `slimits`.
- Over-requested resources → reduce `mem_mb`/`runtime`.
- Running without dry-run → harder to debug DAG/resource errors.

## 7) Lab best practice

- Keep one workflow per project folder.
- Commit `Snakefile`, `config/`, and profile YAML to git.
- Start with 1–2 sample files before launching full cohort jobs.
