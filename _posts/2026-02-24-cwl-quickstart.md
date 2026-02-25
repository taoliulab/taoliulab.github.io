---
layout: post
title: "Tutorial: CWL quickstart"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short starter guide for running **CWL workflows on UB CCR**.

Official references:
- CWL user guide: <https://www.commonwl.org/user_guide/>
- cwltool docs: <https://cwltool.readthedocs.io/en/latest/>
- CCR jobs docs: <https://docs.ccr.buffalo.edu/en/latest/hpc/jobs/>

## 1) Login and create environment

```bash
ssh <CCRUsername>@vortex.ccr.buffalo.edu
module load gcc python
python3 -m venv /projects/academic/<YourGroupName>/venvs/cwl
source /projects/academic/<YourGroupName>/venvs/cwl/bin/activate
pip install --upgrade pip
pip install cwltool
```

Verify:

```bash
cwltool --version
```

## 2) Create a tiny CWL example

Create `hello-tool.cwl`:

```yaml
cwlVersion: v1.2
class: CommandLineTool
baseCommand: echo
inputs:
  message:
    type: string
    inputBinding:
      position: 1
outputs:
  out:
    type: stdout
stdout: hello.txt
```

Create `job.yml`:

```yaml
message: "hello_ccr"
```

Test locally on login node (small test only):

```bash
cwltool hello-tool.cwl job.yml
```

## 3) Run CWL inside a SLURM batch job

Create `run_cwl.sbatch`:

```bash
#!/bin/bash -l
#SBATCH --cluster=ub-hpc
#SBATCH --partition=general-compute
#SBATCH --qos=general-compute
#SBATCH --account=<SlurmAccountName>
#SBATCH --time=01:00:00
#SBATCH --nodes=1
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=4
#SBATCH --mem=8G
#SBATCH --job-name=cwl-test
#SBATCH --output=%x-%j.out
#SBATCH --error=%x-%j.err

module load gcc python
source /projects/academic/<YourGroupName>/venvs/cwl/bin/activate

cwltool hello-tool.cwl job.yml
```

Submit:

```bash
sbatch run_cwl.sbatch
```

## 4) Monitoring

```bash
squeue -u $USER
sacct -j <jobid> --format=JobID,State,Elapsed,ReqMem,MaxRSS
```

## 5) Container notes

Many CWL workflows rely on containerized tools. If your workflow includes `DockerRequirement`, follow CCR policy-supported container options and test a small job first.

## 6) Common issues

- File paths in `job.yml` are wrong (relative path confusion).
- Missing cluster account/partition in batch script.
- Trying large jobs on login node instead of `sbatch`.

## 7) Lab best practice

- Keep CWL files, input YAML, and SLURM scripts in the same project repo.
- Version-control workflow + example input files.
- Start with a tiny validation run before full-scale execution.
