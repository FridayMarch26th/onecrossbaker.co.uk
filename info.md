---
layout: default
title: Important information
description: Food hygiene certification and allergen information for One Cross Baker breads.
variant: page
permalink: /info/
---

I hold a **Level 2 Food Hygiene and Safety for Retail** certificate.

[View my certificate (PDF)]({{ '/assets/files/level_2_Food_Hygiene_and_Safety_for_Retail.pdf' | relative_url }}){:target="_blank" rel="noopener"}
\| [Verify my certificate](https://www.highspeedtraining.co.uk/verify){:target="_blank" rel="noopener"}

## Allergens

{% if site.data.breads and site.data.breads.size > 0 -%}
<table class="allergens">
  <thead>
    <tr><th scope="col">Bread</th><th scope="col">Contains</th></tr>
  </thead>
  <tbody>
    {%- for bread in site.data.breads %}
    <tr>
      <th scope="row">{{ bread.name }}</th>
      <td>{{ bread['contains'] | join: ', ' | default: '—' }}</td>
    </tr>
    {%- endfor %}
  </tbody>
</table>

Everything is made with a ton of care in my domestic kitchen.
{%- else -%}
Details for each bread will appear here before it goes on offer.
{%- endif %}