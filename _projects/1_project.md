---
layout: page
title: deLemus
description: Dynamic Expedition of Leading Mutations in SARS-CoV-2 Spike Glycoproteins.
img: assets/img/deLemus_project/spike.png
importance: 1
category: work
giscus_comments: true
---

Throughout the ongoing COVID-19 pandemic, the continuous genomic evolution of severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) has resulted in the generation of new variants with enhanced transmissibility and immune escape. Being one key target of antibodies, mutations of the spike glycoprotein play a vital role in the trajectory of viral evolution. Here, we present a time-resolved statistical method, dynamic expedition of leading mutations (deLemus), to analyze the evolution dynamics of the spike protein. Together with analysis on single amino acid polymorphism (SAP), we propose an L-index to quantify the mutation strength of each amino acid for unravelling the evolutionary mutation pattern of the spike glycoprotein. The sites of interest (SOIs) with high L-indices are predicted to hold great promise in detecting potential signals of emerging variants.

<br>

<h4 style="text-align: left;"><strong>Spike Protein</strong></h4>
<hr>
The spike glycoprotein of SARS-CoV-2 is a trimeric type I viral fusion protein that binds the virus to the angiotensin-converting enzyme 2 (ACE2) receptor of a host cell. It is composed of 2 subunits: the N-terminal subunit 1 (S1) and C-terminal subunit 2 (S2), within which multiple domains lie. The S1 region facilitates ACE2 binding and is made up of an N-terminal domain (NTD), a receptor-binding domain (RBD), and 2 C-terminal subdomains (CTD1 and CTD2), while the downstream S2 region is responsible for mediating virus-host cell membrane fusion.
<div class="row">
    <div class="mt-3 mt-md-0">
        {% include figure.html path="assets/img/deLemus_project/Domains.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<h4 style="text-align: left;"><strong>Outlined Leading Mutations</strong></h4>
<hr>

<div class="l-page">
    <style>
        .molstar {
            position: relative;
            padding-bottom: 80%;
        }
    </style>
    <link rel="stylesheet" type="text/css" href="https://molstar.org/viewer/molstar.css" />
    <script type="text/javascript" src="https://molstar.org/viewer/molstar.js"></script>

    <div id="viewer-7" class="molstar" style="display: block; margin-left:auto; margin-right:auto; padding-bottom: 80%;"></div>
    <script type="text/javascript">
        molstar.Viewer.create('viewer-7', {
            layoutIsExpanded: false,
            layoutShowControls: false,
            layoutShowRemoteState: false,
            layoutShowSequence: true,
            layoutShowLog: false,
            layoutShowLeftPanel: true,

            viewportShowExpand: true,
            viewportShowSelectionMode: false,
            viewportShowAnimation: false,
        }).then(viewer => {
            viewer.loadSnapshotFromUrl("{{ '/assets/molx/LM_2023_07.molx' | relative_url }}", 'molx');
        });
    </script>
</div>

<div class="caption">
    3D structure powered by AlphaFold2, Colab. This structure demonstrates the leading mutation that we captured at 2023.7.
</div>
