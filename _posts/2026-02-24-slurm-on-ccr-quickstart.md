---
layout: post
title: "Tutorial: SLURM on CCR quickstart"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short, practical guide for new lab members running jobs on the University at Buffalo CCR cluster.

Official references:
- CCR docs (Running Jobs): <https://docs.ccr.buffalo.edu/en/latest/hpc/jobs/>
- CCR example scripts: <https://github.com/ubccr/ccr-examples/tree/main/slurm>

## 1) Login to CCR

```bash
ssh <CCRUsername>@vortex.ccr.buffalo.edu
```

(Use your normal CCR onboarding + DUO flow.)

## 2) Check your available accounts and limits

```bash
slimits
```

This helps you identify valid Slurm account, partition, and QoS values for your group.

## 3) Create a simple batch script

Create a file `job.bash`:

```bash
#!/bin/bash -l
#SBATCH --cluster=ub-hpc
#SBATCH --partition=general-compute
#SBATCH --qos=general-compute
#SBATCH --account=<SlurmAccountName>
#SBATCH --time=02:00:00
#SBATCH --nodes=1
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=8
#SBATCH --mem=32G
#SBATCH --job-name=lab-test
#SBATCH --output=%x-%j.out
#SBATCH --error=%x-%j.err

# Optional: set threads for OpenMP-style apps
export OMP_NUM_THREADS=$SLURM_CPUS_PER_TASK

echo "Running on $(hostname)"
echo "Job ID: $SLURM_JOB_ID"

# Example command (replace with your real workload)
python analysis.py
```

Notes:
- CCR examples use `#!/bin/bash -l` for batch scripts.
- Keep requests realistic (time, CPU, memory) so jobs start sooner.

## 4) Submit and monitor

Submit:

```bash
sbatch job.bash
```

Check queue status:

```bash
squeue -u $USER
```

Check finished-job accounting:

```bash
sacct -j <JobID> --format=JobID,State,Elapsed,ReqMem,MaxRSS
```

Cancel a job:

```bash
scancel <JobID>
```

## 5) Interactive job (when needed)

For short debugging/testing sessions:

```bash
salloc \
  --partition=general-compute \
  --qos=general-compute \
  --nodes=1 \
  --ntasks-per-node=1 \
  --cpus-per-task=8 \
  --mem=32G \
  --time=01:00:00 \
  --no-shell

srun --jobid=<JobID> --export=HOME,TERM,SHELL --pty /bin/bash --login
```

When done:

```bash
exit
scancel <JobID>
```

## 6) Common issues

- Submitting from compute node instead of login node.
- Forgetting to set `--account` to a valid Slurm account.
- Requesting too many resources “just in case” (causes long queue waits).
- Running big jobs interactively instead of using `sbatch`.

## 7) Lab best practice

- Keep each analysis in a project folder with:
  - `job.bash`
  - software environment file (`environment.yml`)
  - clear output/log naming
- Start with a small test job first, then scale up.
