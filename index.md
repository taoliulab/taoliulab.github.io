---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
description: "Tao Liu Lab at Roswell Park: computational genomics, epigenomics, software, publications, and tutorials."
---

Welcome to the main page of Tao Liu's lab page at Roswell Park.

My long-term research interest is to develop and apply computational
approaches for studying transcriptional and epigenetic regulation. My
group at Roswell Park Comprehensive Cancer Center focuses on building
bioinformatics algorithms for single-cell genomics assays to study
gene regulatory mechanisms and the influence of the genetic variations
at cis-regulatory elements. I am maintaining some widely used
bioinformatics algorithms for genomics analysis such as
[MACS](https://macs3-project.github.io/MACS/) for Chromatin
Immunoprecipitation with High-throughput Sequencing. I have close
collaborations with experimentalists, biologists and clinicians in
various fields.

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

