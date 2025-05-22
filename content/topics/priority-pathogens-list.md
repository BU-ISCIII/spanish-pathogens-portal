---
title: "Priority Pathogens List"
description: Priority Pathogens List Developped within PDN
topic: priority-pathogens-list
banner: /topics/banners/topic_priority_list.jpg
banner_caption: "Priority Pathogens List"
menu:
  topics:
    name: Priority Pathogens List
    identifier: priority-pathogens-list
---

This section includes all the relevant information about the Priority Pathogens List developped in the context of the PDN project. You can find the priority pathogen lists in <a target="_blank" href="https://github.com/BU-ISCIII/pdn_priority_pathogens">this Github repo <i class="bi bi-github"></i></a>

## Objectives

The objectives of generating a priority pathogens list are:

<ul class="mb-4">
  <li class="mb-2">Aggregate pathogen prioritization lists from leading public health and research organizations.</li>
  <li class="mb-2">Provide a unified reference with consistent taxonomy and annotation.</li>
  <li class="mb-2">Support pathogen surveillance, pandemic preparedness, and biosecurity efforts.</li>
  <li class="mb-2">Make prioritization data machine-readable, as many official lists are only available in formats (PDFs or websites) that are not readily accessible for automated analysis.</li>
</ul>

## Methodology

### Taxonomic standardization

<ul class="mb-4">
  <li class="mb-2">Pathogens are named using scientific species names whenever possible.</li>
  <li class="mb-2">When species-level resolution is not feasible, the genus name is used.</li>
  <li class="mb-2">Viral naming follows ICTV (International Committee on Taxonomy of Viruses) recommendations.</li>
  <li class="mb-2">Additional or common names are listed under the <code>also_known_as</code> field.</li>
</ul>

### Data sources

The prioritization list integrates information from international and national agencies, using their publicly available priority lists. Each source is referenced below:

<table class="table table-bordered table-hover mb-5">
  <thead class="table-light">
    <tr>
      <th>Organization</th>
      <th>Acronym</th>
      <th>Link</th>
      <th>List Name</th>
      <th>Source URLs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>National Institute of Allergy and Infectious Diseases</td>
      <td>NIAID</td>
      <td><a href="https://www.niaid.nih.gov/" target="_blank">niaid.nih.gov</a></td>
      <td>NIAID Biodefense Pathogens, Research, Wiriya's document</td>
      <td>
        <a href="https://www.niaid.nih.gov/research/niaid-biodefense-pathogens" target="_blank">[1]</a>,
        <a href="https://www.niaid.nih.gov/research-areas" target="_blank">[2]</a>,
        <a href="https://docs.google.com/document/d/1RY7u4TiTzBV_1T7Rthpn2gdU5pBwPnOc/edit" target="_blank">[3]</a>
      </td>
    </tr>
    <tr>
      <td>European Centre for Disease Prevention and Control</td>
      <td>ECDC</td>
      <td><a href="https://www.ecdc.europa.eu/en" target="_blank">ecdc.europa.eu</a></td>
      <td>Disease-based list</td>
      <td><a href="https://www.ecdc.europa.eu/en/all-topics" target="_blank">Link</a></td>
    </tr>
    <tr>
      <td>World Health Organization</td>
      <td>WHO</td>
      <td><a href="https://www.who.int/" target="_blank">who.int</a></td>
      <td>WHO priority pathogen lists (scientific framework, bacteria, fungi)</td>
      <td>
        <a href="https://www.who.int/publications/m/item/pathogens-prioritization-a-scientific-framework-for-epidemic-and-pandemic-research-preparedness" target="_blank">[1]</a>,
        <a href="https://www.who.int/publications/i/item/9789240093461" target="_blank">[2]</a>,
        <a href="https://www.who.int/publications/i/item/9789240060241" target="_blank">[3]</a>
      </td>
    </tr>
    <tr>
      <td>Africa Centres for Disease Control and Prevention</td>
      <td>AFRICACDC</td>
      <td><a href="https://africacdc.org/" target="_blank">africacdc.org</a></td>
      <td>Epidemic-prone diseases prioritization</td>
      <td><a href="https://africacdc.org/download/risk-ranking-and-prioritization-of-epidemic-prone-diseases/" target="_blank">Link</a></td>
    </tr>
    <tr>
      <td>Centers for Disease Control and Prevention (USA)</td>
      <td>CDC</td>
      <td><a href="https://www.cdc.gov/" target="_blank">cdc.gov</a></td>
      <td>AMR Threats Report 2021-2022</td>
      <td><a href="https://www.cdc.gov/antimicrobial-resistance/media/pdfs/antimicrobial-resistance-threats-update-2022-508.pdf" target="_blank">Link</a></td>
    </tr>
  </tbody>
</table>

<div class="row text-left mb-5">
  <div class="col-md-6">
      <img height="400" src="/img/pathogens_perlist.png" alt="pathogens_perlist">
      <div class="small text-muted mt-1">Figure 1: Number of pathogens found in the lists of each organization. A total of 198 pathogens from 98 families were included.</div>
  </div>
  <div class="col-md-6">
      <img height="400" src="/img/venn_all.png" alt="venn_all">
      <div class="small text-muted mt-1">Figure 2: Venn diagram of the pathogens shared between NIAID, WHO and ECDC</div>
  </div>
  <div class="col-md-8">
      <img height="400" src="/img/pathogen_type_all.png" alt="pathogens_pertype">
      <div class="small text-muted mt-1">Figure 3: Number of pathogens per type.</div>
  </div>
</div>

<div>
You can consult the <a href="https://docs.google.com/spreadsheets/d/1nrG329whDaeVv8BpocWUuSc-lgv-TJVf6RIxW3Bd8jg/edit?usp=sharing">live Google Sheet</a> used for this repository.
</div>

## Priority Type Classification

Each pathogen is categorized into one or more "priority types", based on its inclusion in the above lists. These allow grouping pathogens by relevance across thematic areas.

Unique priority types used:

<code>
<ul class="mb-4">
  <li class="mb-2">Pandemic preparedness</li>
  <li class="mb-2">Biodefense/Bioterrorism</li>
  <li class="mb-2">Vaccine-preventable</li>
  <li class="mb-2">STI</li>
  <li class="mb-2">AMR/Nosocomial infection</li>
  <li class="mb-2">Animal disease</li>
  <li class="mb-2">Neglected Tropical Diseases</li>
  <li class="mb-2">Other</li>
</ul>
</code>

<div class="mb-3">
<strong>Note</strong> that pathogens may belong to multiple categories simultaneously.
</div>

<div class="text-left mb-3">
  <img height="400" src="/img/priority_type_all.png" alt="priority_type_all">
  <div class="small text-muted mt-1">Figure 4: Number of pathogens in each of the priority types, among the 198 in the list.</div>
</div>

### Prioritization logic

#### Inclusion criteria

<ul class="mb-4">
  <li class="mb-2">
    Included if the pathogen appears in at least <strong>two of the following global health agency lists</strong>: WHO, NIAID, ECDC.
    <ul class="mt-2">
      <li class="mb-2">
        <strong>Note:</strong> Fungal pathogens are only prioritized by WHO and NIAID and are not present in ECDC or Africa CDC lists.
      </li>
    </ul>
  </li>
  <li class="mb-2">
    Additionally, the pathogen must be listed under at least <strong>two distinct priority categories</strong>, excluding "Animal disease".
  </li>
</ul>

#### Score and ranking

Each pathogen is assigned a composite --priority score--, calculated based on:

<ul class="mb-4">
  <li class="mb-2">Number of appearances in key organizational lists (WHO, NIAID, ECDC) ×1</li>
  <li class="mb-2">Number of appearances in broader organizational sets (WHO, NIAID, ECDC, AFRICACDC) ×2</li>
  <li class="mb-2">Number of different priority types (excluding "Animal disease") ×1</li>
  <li class="mb-2">Whether the pathogen has been detected in wastewater monitoring ×1</li>
  <li class="mb-2">
    Additional adjustment for underepresentation:
    <ul class="mt-2">
      <li>Fungi: +3</li>
      <li>Protozoan parasites: +4</li>
    </ul>
  </li>
</ul>

This score is stored in the field `priority_score`.

The full ranked list is available in `complete_priority_pathogens.json`, including the computed priority score and the derived `priority_order`.

#### Final selection

<ul class="mb-4">
  <li class="mb-2">A total of <strong>50 pathogens</strong> from <strong>33 families</strong> were retained after filtering.</li>
  <li class="mb-2">From this list, a subset of <strong>22 pathogens</strong> is selected for PDN priority consideration, based on the inclusion criteria.</li>
  <li class="mb-2">Pathogens with a <strong>priority score ≥ 12</strong> are marked with <code>highest_priority: true</code>.</li>
</ul>

<div class="row text-left mb-5">
  <div class="col-md-6">
      <img height="400" src="/img/pathogen_type_proposed.png" alt="pathogen_type_proposed">
      <div class="small text-muted mt-1">Figure 5: Number of pathogens per type for the 50 pathogens in the final selection.</div>
  </div>
  <div class="col-md-6">
      <img height="400" src="/img/venn_proposed.png" alt="venn_proposed">
      <div class="small text-muted mt-1">Figure 6: Venn diagram of the pathogens shared between NIAID, WHO and ECDC among the 50 pathogens in the final selection</div>
  </div>
  <div class="col-md-9">
      <img height="500" src="/img/priority_type_proposed.png" alt="priority_type_proposed">
      <div class="small text-muted mt-1">Figure 7: Number of pathogens found in each priority type for the 50 pathogens in the final selection.</div>
  </div>
</div>
