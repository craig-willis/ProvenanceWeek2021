---
layout: page
title: IPAW
---

The International Provenance and Annotation Workshop (IPAW) is a biannual workshop that is concerned with issues of data provenance, data derivation, and data annotation. It brings together computer scientists from different areas and provenance users to discuss open problems related to the provenance of computation and non-computational artifacts.

The proceedings for IPAW have been published by Springer since 2008. You can find them here: [https://link.springer.com/conference/ipaw](https://link.springer.com/conference/ipaw).


### Organizers

{% assign pcchair = site.data.organizers.chairs | where: "role", "IPAW PC chair" | first %}
* **{{ pcchair.name }}** ({{ pcchair.affiliation }}) - PC Chair

{% if site.data.ipaw.accepted_papers.size > 0 %}
### Accepted Papers

2021 IPAW papers will be published together with 2020 papers in the 2021 Springer proceedings. For now preprints of accepted papers, if provided by the authors, are linked below.

{% for p in site.data.ipaw.accepted_papers %}
{% assign authors = p.authors | map: 'name' %}
* **{{ p.title }}** (*{{ authors | join: ', ' }}*) {% if p.preprint %}**preprint**: [{{ p.preprint }}]({{ p.preprint }}){% endif %}
{% endfor %}
{% endif %}

### Program Committee

{% for pc in site.data.ipaw.pc %}
* **{{ pc.name }}** ({{ pc.affiliation }})
{% endfor %}
