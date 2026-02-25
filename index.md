---
layout: home
description: "Tao Liu Lab at Roswell Park: computational genomics, epigenomics, software, publications, and tutorials."
---

Welcome to the Tao Liu Lab at Roswell Park Comprehensive Cancer Center.

We develop computational methods and open-source software to study transcriptional and epigenetic regulation, with a focus on cancer biology, single-cell genomics, and AI-enabled genomics data reuse.

## Research at a glance

- Algorithm development for ChIP-seq, CUT&RUN, ATAC-seq, and single-cell assays
- Regulatory genomics in cancer and developmental systems
- AI agent development for genomics data reuse and metadata standardization
- Scalable, reproducible analysis workflows and data infrastructure

## Quick links

- [Research]({{ site.baseurl }}{% link Research.md %})
- [Publications]({{ site.baseurl }}{% link Publications.md %})
- [Software]({{ site.baseurl }}{% link Software.md %})
- [Tutorials]({{ site.baseurl }}{% link Tutorial.md %})
- [People]({{ site.baseurl }}{% link People.md %})

## Latest News

<ul>
{% assign now_ts = "now" | date: "%s" | plus: 0 %}
{% assign one_year_secs = 31536000 %}
{% assign shown = 0 %}
{% for post in site.posts %}
  {% assign post_ts = post.date | date: "%s" | plus: 0 %}
  {% assign age = now_ts | minus: post_ts %}
  {% unless post.categories contains "Tutorials" %}
    {% if age <= one_year_secs and shown < 5 %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <small>({{ post.date | date: "%Y-%m-%d" }})</small></li>
      {% assign shown = shown | plus: 1 %}
    {% endif %}
  {% endunless %}
{% endfor %}
</ul>

## Featured Software

- [MACS3](https://github.com/macs3-project/MACS)
- [HMMRATAC](https://github.com/LiuLabUB/HMMRATAC)
- [MAESTRO](https://github.com/liulab-dfci/MAESTRO)
- More tools: [Software]({{ site.baseurl }}{% link Software.md %})

## Join / Contact

We welcome collaborations and applications from students and postdocs interested in computational biology, gene regulation, single-cell genomics, and AI for biomedical data analysis.

- Contact: [tao.liu@roswellpark.org](mailto:tao.liu@roswellpark.org)
- Lab overview: [Research]({{ site.baseurl }}{% link Research.md %})
