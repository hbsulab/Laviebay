---
layout: page
title: Solid State Materials
description: 
img: assets/img/solid_state/Solid_state.jpg
importance: 2
category: work
giscus_comments: true
---

With an increasing demand for advanced functional materials in various applications, the molecular simulation of these materials has become a critical area of research.  In particular, the study of perovskite materials and phase-change materials offers significant potential for the development of novel devices and technologies. Consequently, there is a growing need for efficient and accurate modeling methodologies to explore the underlying mechanisms governing their properties and performance. 

<br>

<h4 style="text-align: left;"><strong>Ge(SbTe<sub>2</sub>)<sub>2</sub> model</strong></h4>
<hr>

<div class="l-page">
    <style>
        .molstar {
            position: relative;
            padding-bottom: 60%;
        }
    </style>
    <link rel="stylesheet" type="text/css" href="https://molstar.org/viewer/molstar.css" />
    <script type="text/javascript" src="https://molstar.org/viewer/molstar.js"></script>

    <div id="viewer-2" class="molstar" style="display: block; margin-left:auto; margin-right:auto; padding-bottom: 60%;"></div>
    <script type="text/javascript">
        molstar.Viewer.create('viewer-2', {
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
            viewer.loadSnapshotFromUrl("{{ 'assets/molx/Solid_state.molx' | relative_url }}", 'molx');
        });
    </script>
</div>

<br>

<h4 style="text-align: left;"><strong>Our Tasks</strong></h4>
<hr>

<div class="row">
    <div class="col-lg-7">
        Molecular dynamics (MD) simulations are a powerful tool that provides in-depth insights into the behavior of functional materials at the atomic level.  By analyzing the structures and developing more efficient and accurate modeling methodologies and applying them to specific functional materials, this research aims to contribute to the development of novel devices and technologies.  This thesis consists of three parts.  <br>
    </div>
    <div class="col-lg-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/solid_state/trj.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The first part is the background study and literature review on perovskite and Ge-Sb-Te functional materials and existing approaches for the molecular simulation.  <br>

The second part focuses on analysis and modelling based on simulation results, including three works: <br>
<strong>1)</strong> complex evolution unveiling for mixed perovskite precursors, <br>
<strong>2)</strong> solid-state transformation simulation for cesium lead halide perovskites, <br>
<strong>3)</strong> unravelling the atomistic transition mechanism in Ge-Sb-Te phase-change materials.  <br>

The third part is, by analysing the structures and developing more efficient and accurate modeling methodologies and applying them to specific functional materials, the insights gained from this research aims to contribute to the development of novel devices and technologies.



