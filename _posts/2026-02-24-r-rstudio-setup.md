---
layout: post
title: "Tutorial: R and RStudio setup"
date: 2026-02-23 09:00:00 -0500
categories: Tutorials
---

This tutorial is for setting up R and RStudio on your **own laptop** (MacBook first).

Official references:
- CRAN macOS R installers: <https://cran.r-project.org/bin/macosx/>
- RStudio Desktop download: <https://posit.co/download/rstudio-desktop/>

## 1) Check your Mac architecture

```bash
uname -m
```

- `arm64` → Apple Silicon (M1/M2/M3/M4 and newer)
- `x86_64` → Intel Mac

## 2) Install R (from CRAN)

1. Open CRAN macOS page: <https://cran.r-project.org/bin/macosx/>
2. Download the correct installer for your architecture:
   - Apple Silicon: `R-*-arm64.pkg`
   - Intel: `R-*-x86_64.pkg`
3. Run the `.pkg` installer and finish setup.

Verify in Terminal:

```bash
R --version
```

## 3) Install RStudio Desktop

1. Download from Posit: <https://posit.co/download/rstudio-desktop/>
2. Install RStudio Desktop.
3. Launch RStudio and confirm it detects your R installation.

## 4) First-time setup in RStudio

Open RStudio Console and run:

```r
install.packages(c("tidyverse", "data.table", "remotes"))
```

Set a CRAN mirror when prompted.

## 5) Create a project (recommended workflow)

In RStudio:
- **File → New Project**
- choose a dedicated folder per project
- keep scripts/data/results together

This helps reproducibility and collaboration.

## 6) Optional: project-local package management with `renv`

Inside a project, run:

```r
install.packages("renv")
renv::init()
```

After installing/updating packages:

```r
renv::snapshot()
```

A collaborator can restore the same package set with:

```r
renv::restore()
```

## 7) Common issues

- RStudio says “R not found”:
  - install/reinstall R from CRAN first, then restart RStudio.
- Package install fails on macOS:
  - update to current R version first,
  - then retry package install.
- Apple Silicon users with old Intel-only package binaries:
  - update R and packages; avoid mixing very old package builds.

## 8) Lab recommendation

Use **one RStudio Project per study** and use `renv` for reproducibility before sharing analysis code.
