---
layout: post
title: "Tutorial: Miniforge setup for bioinformatics"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This is a short, practical guide for new lab members setting up Miniforge on Linux or macOS.

Official references:
- Miniforge docs and releases: <https://github.com/conda-forge/miniforge>

## 1) Check your architecture

```bash
uname
uname -m
```

Expected architecture values:
- Linux Intel/AMD: `x86_64`
- Linux ARM64: `aarch64`
- macOS Intel: `x86_64`
- macOS Apple Silicon (M1/M2/M3/M4 and newer): `arm64`

## 2) Download and run the official installer

### Linux (recommended command from Miniforge docs)

```bash
wget -O Miniforge3.sh "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3.sh
```

### macOS (recommended command from Miniforge docs)

```bash
curl -fsSLo Miniforge3.sh "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-$(uname -m).sh"
bash Miniforge3.sh
```

During interactive install:
- use default install location (recommended)
- allow installer to run `conda init`

Then close and reopen terminal.

## 3) Confirm installation

```bash
conda --version
mamba --version
```

If commands are not found:

```bash
~/miniforge3/bin/conda init
```

Restart terminal after that.

## 4) Create your lab environment

```bash
mamba create -n lab python=3.11 -y
conda activate lab
mamba install -y numpy pandas scipy matplotlib jupyterlab
```

## 5) Daily usage

```bash
conda activate lab
conda env list
conda deactivate
```

## 6) Best practice for lab work

- Do **not** install project dependencies into `base`.
- Use one conda environment per project.
- Export an environment file when sharing workflows:

```bash
conda env export --no-builds > environment.yml
```

Recreate the same environment elsewhere:

```bash
mamba env create -f environment.yml
```

## 7) Optional cleanup / shell behavior

Disable auto-activating `base` at every terminal start:

```bash
conda config --set auto_activate_base false
```

If shell activation is still broken:

```bash
conda init bash   # Linux bash users
conda init zsh    # macOS default shell
```

Then restart terminal.
