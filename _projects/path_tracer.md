---
layout: page
title: Volumetric Path Tracing
description: MSI 882 Path Tracing - Final Project
img: assets/img/projects/path_tracer/final_composition.png
importance: 1
category: formation
---

At École des Technologies Supérieures (ETS), I had an amazing course on Path Tracing by Adrien Gruson. 

In my course, I was able to grasp many concepts related to the state of the art. 

At the end, we were ask to implement a state-of-the-art implementation on Path Tracing. We choose to implement a Spectral Volumetric Rendering for Heteregenous Media using NEE MIS based on [A null-scattering path integral formulation of light transport](https://dl.acm.org/doi/pdf/10.1145/3306346.3323025)

<div class="row-sm mt-3 mt-md-0 pb-2">
    <center>
    {% include figure.html path="assets/img/projects/path_tracer/final_composition.png" title="Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}
    
    Final Image Composition

    </center>
</div>

<div class="row">
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>

            {% include figure.html path="assets/img/projects/path_tracer/homo_nomis_vs_mis.png" title="Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}
            
            Homogeneous Volumetric No MIS vs MIS
        
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>

            {% include figure.html path="assets/img/projects/path_tracer/homo_spectral_nomis_vs_mis.png" title="Spectral Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}

            Spectral Homogeneous No MIS vs MIS
        
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/path_tracer/hetero_spectral.png" title="Heterogeneous Spectral" class="img-fluid rounded z-depth-1" %}

            Heterogeneous Spectral with Different Parameters

        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2" style="text-align: center">
        <center>

                {% include figure.html path="assets/img/projects/path_tracer/hetero_spectral_mis_nee.png" title="Heterogeneous Spectral MIS" class="img-fluid rounded z-depth-1 center" %}

            Heterogeneous MIS Spectral with Different Parameters
            
        </center>

    </div>
</div>