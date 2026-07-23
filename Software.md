---
layout: page
title: "Software"
permalink: /Software/
description: "Open-source software and analysis pipelines developed by the Tao Liu Lab."
---

# Open-source software

We develop software for epigenomics, single-cell analysis, and biomedical data reuse. Source code, documentation, and issue trackers are linked below.

## Core tools

### [MACS3](https://github.com/macs3-project/MACS)

MACS3 is a peak caller for ChIP-seq and other DNA enrichment assays. It models local background signal to identify enriched genomic regions. See the [documentation](https://macs3-project.github.io/MACS/) for installation and command-line usage.

### [HMMRATAC](https://github.com/LiuLabUB/HMMRATAC)

HMMRATAC identifies open chromatin regions from paired-end ATAC-seq data with a hidden Markov model. The current implementation is available through the [`macs3 hmmratac`](https://macs3-project.github.io/MACS/docs/hmmratac.html) command; the original Java repository is retained for reference.

### [MAESTRO](https://github.com/liulab-dfci/MAESTRO)

MAESTRO is an analysis workflow for single-cell RNA-seq and ATAC-seq. It covers processing, quality control, clustering, cell-type annotation, and regulatory analysis from raw sequencing data.

### [RetrieverApp](https://github.com/RetrieverApp/retriever_app)

RetrieverApp collects publications and linked records from PubMed, GEO, SRA, dbGaP, and ClinicalTrials.gov. It produces editable reports for investigators and large research collaborations.

## Genomics analysis pipelines

Our [Snakemake pipeline repository](https://github.com/macs3-project/genomics-analysis-pipelines) contains experimental workflows built around MACS3:

- [Bulk ChIP-seq](https://github.com/macs3-project/genomics-analysis-pipelines/tree/master/Bulk-ChIP-seq)
- [Bulk ATAC-seq](https://github.com/macs3-project/genomics-analysis-pipelines/tree/master/Bulk-ATAC-seq)
- [Bulk RNA-seq](https://github.com/macs3-project/genomics-analysis-pipelines/tree/master/Bulk-RNA-seq)

## Web platforms and databases

### [Cistrome](http://cistrome.org/ap/root)

Cistrome provides web-based tools for integrative analysis of transcriptional and epigenetic regulation.

### [Cistrome Data Browser](http://cistrome.org/db/)

Cistrome Data Browser makes uniformly processed human and mouse ChIP-seq and chromatin-accessibility datasets available for search, visualization, and reuse.
