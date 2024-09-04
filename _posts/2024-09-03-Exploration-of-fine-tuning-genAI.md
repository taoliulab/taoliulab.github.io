---
layout: post
title:  "Exploration of fine-tuning genAI"
date:   2024-09-03 16:10:00 -0500
categories: Blog
---

In the summer of 2024, Trey Hutson, a college student, and Jonathan Li, a high school student,  joined my lab for their summer intern projects. I decided to make a team to work on a quick AI (generative AI) project so that all of us can learn something new together. Our programmer, Philippa Doherty, built an automatic pipeline to retrieve the relevant publications and the associated publicly-available datasets of given PMIDs or Grant IDs from NCBI databases. However, annotating the genomics data type for datasets submitted to NCBI GEO and SRA requires downloading metadata from these repositories, carefully reviewing the relevant data fields, and making informed judgments when data types are uncommon or mislabeled. In many cases, accurate labeling requires a comprehensive manual review of various metadata fields. To avoid this tedious work (and to be a good lazy person), we planned to fine-tune a Large Language Model to help us review the metadata. The project is a typical application for LLM -- to classify (or perhaps predict) the input data and assign labels.

# Method

## The pick of LLM

## The workflow

## The training data

## The fine-tuned model

## The source code

# Result 

# Discussion
