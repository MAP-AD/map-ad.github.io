---
layout: main
title: Home
---

## Welcome to the MAP tools wiki!

This is a collection of tools put together to process/analyse data from the multi-'omics atlas project (MAP).

The MAP tools wiki is designed as a central resource to help researchers navigate and utilise tools developed/used for MAP. Here, you will find documentation, user guides, and best practices for each tool.

### Table of Contents
- [Getting Started](#getting-started)
- [Tools table](#tools-table)
- [Contributing](#contributing)
- [Support](#support)
- [Latest Updates](#latest-updates)
- [FAQs](#faqs)
- [Contact Information](#contact-information)

### Getting Started

To begin, explore the tools table below to find the tool that best suits your needs. Each entry includes a brief description and a link to the documentation.

### Tools table

| Tool | Description | GitHub |
|------|-------------|------|
{% for page in site.pages -%}
{% if page.tool -%}
| [{{ page.name }}]({{page.url}}) | {{ page.description }} | [{{ page.github }}]({{ page.github }}) |
{% endif -%}
{% endfor %}

### Contributing

We welcome contributions. If you have developed a tool used for MAP or have improvements to suggest to one, please refer to our [contribution guidelines](contributing.md) for more information.

### Support

If you encounter any issues with the site or have questions, please open an issue on our [GitHub repository](https://github.com/MAP-AD/map-ad.github.io). Likewise any issues with the tools themselves should be reported to the respective tool repository. This can be found in the tool's documentation page.

Happy analysing!

### Latest Updates

{% for page in site.pages limit:5 %}
{% if page.layout == 'update' %}
- [**{{page.date}}** *{{ page.title }}*]({{ page.url }})
{% endif %}
{% endfor %}

### Contact Information

<img class=inline_image src="/assets/img/Michael.png" width=75px /> Site Developer: [Michael Thomas](mailto:michael.thomas21@imperial.ac.uk)