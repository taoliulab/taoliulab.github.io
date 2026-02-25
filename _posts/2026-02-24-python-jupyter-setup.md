---
layout: post
title: "Tutorial: Python and Jupyter setup"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short starter guide for using Python and Jupyter on UB CCR.

Official references used for this tutorial:
- CCR Python docs: <https://docs.ccr.buffalo.edu/en/latest/howto/python/>
- CCR jobs docs: <https://docs.ccr.buffalo.edu/en/latest/hpc/jobs/>
- Jupyter install docs: <https://jupyter.org/install>

## 1) Login and load CCR Python module

```bash
ssh <CCRUsername>@vortex.ccr.buffalo.edu
module load gcc python
which python
```

Important: On CCR, **always load `gcc python` first** before creating environments.

## 2) Create a virtual environment in project space

Use your group project directory (not home directory):

```bash
module load gcc python
python3 -m venv /projects/academic/<YourGroupName>/venvs/lab-py
source /projects/academic/<YourGroupName>/venvs/lab-py/bin/activate
```

Then upgrade pip and install basics:

```bash
pip install --upgrade pip
pip install jupyterlab ipykernel numpy pandas scipy matplotlib
```

## 3) Register a Jupyter kernel

```bash
module load gcc python
source /projects/academic/<YourGroupName>/venvs/lab-py/bin/activate
python3 -m ipykernel install --user --name lab-py --display-name "Python (lab-py)"
```

After this, your kernel should appear in Jupyter sessions on CCR (you may need to refresh/restart the session).

## 4) Start JupyterLab (interactive use)

For local testing on a compute allocation:

```bash
module load gcc python
source /projects/academic/<YourGroupName>/venvs/lab-py/bin/activate
jupyter lab --no-browser --ip=0.0.0.0 --port=8888
```

In practice on CCR, many users launch Jupyter through Open OnDemand and then choose the kernel created above.

## 5) Batch-first recommendation for heavy workloads

Use notebooks for exploration, but run heavy training/analysis as Slurm batch jobs for better resource usage.

Example batch skeleton:

```bash
#!/bin/bash -l
#SBATCH --cluster=ub-hpc
#SBATCH --partition=general-compute
#SBATCH --qos=general-compute
#SBATCH --account=<SlurmAccountName>
#SBATCH --time=04:00:00
#SBATCH --nodes=1
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=8
#SBATCH --mem=32G
#SBATCH --job-name=py-job
#SBATCH --output=%x-%j.out

module load gcc python
source /projects/academic/<YourGroupName>/venvs/lab-py/bin/activate
python train.py
```

Submit with:

```bash
sbatch job.bash
```

## 6) Common pitfalls (CCR-specific)

- Creating venv before `module load gcc python` (can break kernels).
- Installing large packages into home directory and running out of quota.
- Using system Python from login node instead of CCR module Python.
- Expecting every package (especially GPU-heavy stacks) to install cleanly with `pip`.

For complex GPU/ML stacks, follow CCR guidance (EasyBuild or container workflow).

## 7) Quick maintenance commands

```bash
# activate env
source /projects/academic/<YourGroupName>/venvs/lab-py/bin/activate

# freeze package versions
pip freeze > requirements.txt

# remove an old kernel
jupyter kernelspec list
jupyter kernelspec uninstall lab-py
```
