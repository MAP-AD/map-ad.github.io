---
layout: main
title: Home
---

## Welcome to the MAP tools wiki!

### About MAP

The UK DRI Multi-‘omics Atlas Project is an open resource dedicated to the comprehensive, multi-’omic mapping of the cellular pathology of Alzheimer’s disease over representative stages in its evolution (MAP AD).

For detailed information about MAP initiative and its objectives, please visit the [official MAP website](https://map-ad.org).

### Purpose of This Wiki

This website serves as a living document, providing an institutional memory and a collaborative platform for sharing the tools, scripts, and workflows developed under the MAP project. It is designed to support MAP researchers by providing:

- **Documentation**: User guides, best practices, and instructions for various tools created as part of MAP.
- **Scripts and Pipelines**: A repository for data processing/analysis scripts and workflows not documented elsewhere.
- **Community Contributions**: A space where members of the MAP research community can share their tools, scripts, and improvements.

This wiki aims to centralise resources to help users effectively utilise MAP tools and scripts. While it does not replace the official documentation of comprehensive tool, it serves as a convenient hub to navigate the array of resources and contributions within the project. Furthermore it is a location for documentation for smaller tools and scripts not provided elsewhere.

---

### Table of Contents
- [Getting Started](#getting-started)
- [Tools table](#tools-table)
- [Contributing](#contributing)
- [Support](#support)
- [Latest Updates](#latest-updates)
- [FAQs](#faqs)
- [Contact Information](#contact-information)

### Getting Started

To begin, explore the tools table below. Each entry includes a brief description of each tool/script and a link to the documentation page and github - if relevent - where you can find more details about its usage. The documentation pages are also available in the sidebar for easy navigation.

### Tools table

| Tool | Description | GitHub |
|------|-------------|------|
{% for page in site.pages -%}
{% if page.tool -%}
| [{{ page.name }}]({{page.url}}) | {{ page.description }} | [{{ page.github }}]({{ page.github }}) |
{% endif -%}
{% endfor %}

### Contributing

We encourage and welcome contributions from the MAP community. Whether you’ve developed a new tool, improved an existing one, or have feedback on the documentation, we would love your input. Please refer to our [contribution guidelines](contributing.md) to learn how.

### Support

If you have questions, encounter technical issues with the site, or need assistance with any of the tools, you can open an issue on our [GitHub repository](https://github.com/MAP-AD/map-ad.github.io). For tool-specific issues, please refer to the respective tool's GitHub repository, which is linked in the tool's documentation.

### Latest Updates

{% for page in site.pages limit:5 %}
{% if page.layout == 'update' %}
- [**{{page.date}}** *{{ page.title }}*]({{ page.url }})
{% endif %}
{% endfor %}

---

### Frequently Asked Questions (FAQs)

#### 1. **Who can contribute to the MAP tools wiki?**
Anyone within the MAP research community or external collaborators interested in contributing to the project can participate. Simply follow our [contribution guidelines](contributing.md) for more details.

#### 2. **What should I do if I find a bug?**
"Please report any bugs directly on the tool’s GitHub repository by creating an issue. If there isn't one, contact the maintainer listed at the top of the relevant documentation."

#### 3. **Where can I find detailed documentation for a tool?**
Each tool has its own dedicated page in the [Tools Table](#tools-table) above, which links to its respective documentation and GitHub repository for further details.

---

### Contact Information

<img class="inline_image" src="/assets/img/Michael.png" width="75px" alt="Site Developer Photo" />  
**Michael Thomas - Site Developer**  
[michael.thomas21@imperial.ac.uk](mailto:michael.thomas21@imperial.ac.uk)