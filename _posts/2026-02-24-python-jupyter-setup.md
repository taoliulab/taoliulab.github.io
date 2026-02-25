---
layout: post
title: "Tutorial: Python and Jupyter setup"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This tutorial is for setting up Python + Jupyter on your **own laptop** (especially MacBook) using **uv**.

Official references:
- uv installation: <https://docs.astral.sh/uv/getting-started/installation/>
- uv projects guide: <https://docs.astral.sh/uv/guides/projects/>
- Jupyter install: <https://jupyter.org/install>

## 1) Install `uv`

### macOS / Linux (official installer)

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

If you use Homebrew on macOS:

```bash
brew install uv
```

Restart terminal, then verify:

```bash
uv --version
```

## 2) Install Python with `uv`

```bash
uv python install 3.11
```

You can check installed Python versions:

```bash
uv python list
```

## 3) Create a project and virtual environment

```bash
mkdir lab-python
cd lab-python
uv init
uv venv --python 3.11
source .venv/bin/activate
```

## 4) Install Jupyter and common scientific packages

```bash
uv pip install jupyterlab ipykernel numpy pandas scipy matplotlib
```

## 5) Register a Jupyter kernel for this environment

```bash
python -m ipykernel install --user --name lab-python --display-name "Python (lab-python)"
```

## 6) Start JupyterLab

```bash
jupyter lab
```

Open the URL shown in terminal (usually `http://localhost:8888/...`).

## 7) Daily workflow

```bash
cd ~/path/to/lab-python
source .venv/bin/activate
jupyter lab
```

When done:

```bash
deactivate
```

## 8) Share/reproduce environment

Export dependencies:

```bash
uv pip freeze > requirements.txt
```

Set up on another machine:

```bash
uv python install 3.11
uv venv --python 3.11
source .venv/bin/activate
uv pip install -r requirements.txt
```

## 9) Common issues

- `uv: command not found` → restart terminal, then re-check PATH.
- Wrong Python version in notebook → activate `.venv` and re-run `ipykernel install`.
- Package conflicts → create a fresh project folder and a new `.venv`.

## 10) Lab recommendation

Use **one project = one `.venv`**. This keeps dependencies clean and reproducible for collaboration.
