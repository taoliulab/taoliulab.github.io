---
layout: post
title: "Tutorial: Miniforge setup for bioinformatics"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short setup guide for new lab members.

Miniforge gives you a clean Python/R package environment manager (`conda` + `mamba`) on Linux and macOS.

## 1) Install Miniforge

### Linux

```bash
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh
bash Miniforge3-Linux-x86_64.sh
```

### macOS (Intel)

```bash
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-x86_64.sh
bash Miniforge3-MacOSX-x86_64.sh
```

### macOS (Apple Silicon, M1/M2/M3)

```bash
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh
bash Miniforge3-MacOSX-arm64.sh
```

When asked, choose:
- install to default path (recommended)
- allow installer to run `conda init`

Then close and reopen your terminal.

## 2) Confirm installation

```bash
conda --version
mamba --version
```

If these commands fail, run:

```bash
source ~/miniforge3/bin/activate
conda init
```

Then restart terminal.

## 3) Create a lab environment

Use one environment per project.

```bash
mamba create -n lab python=3.11 -y
conda activate lab
```

Install common packages:

```bash
mamba install -y numpy pandas scipy matplotlib jupyterlab
```

## 4) Daily usage

Activate environment:

```bash
conda activate lab
```

List environments:

```bash
conda env list
```

Deactivate:

```bash
conda deactivate
```

Update packages in current environment:

```bash
mamba update --all -y
```

## 5) Recommended lab practice

- Do not install project dependencies into `base`.
- Keep one environment per project (for reproducibility).
- Export environment file when sharing pipelines:

```bash
conda env export --no-builds > environment.yml
```

Recreate from file:

```bash
mamba env create -f environment.yml
```

## 6) Quick troubleshooting

If dependency solving is slow, use `mamba` instead of `conda`.

If shell activation does not work, run:

```bash
conda init bash   # Linux / bash users
conda init zsh    # macOS default shell
```

Then restart terminal.

If you accidentally broke `base`, create a fresh environment and continue there.
