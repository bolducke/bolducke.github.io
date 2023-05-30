---
layout: page
title: MTI882 - Path Tracing
description: MTI 882 Path Tracing - Final Project
img: assets/img/projects/mti882_path_tracer/final_composition.png
importance: 1
category: formation
---

At École des Technologies Supérieures (ETS), I had an amazing course on Path Tracing by Adrien Gruson. We got a really up-to-date overview of the current development and state-of-the-art algorithm in path tracing.

For the final project, we were ask to implement new feature and compose a scene. We choose to do volumetric path tracing and implement a Spectral Volumetric Rendering for Heteregenous Media using NEE MIS based on [A null-scattering path integral formulation of light transport](https://dl.acm.org/doi/pdf/10.1145/3306346.3323025). The picture below showcase the feature that I implement with [Matthieu BEAUD](https://www.linkedin.com/in/matthieu-beaud/) for our project.

<div class="row-sm mt-3 mt-md-0 pb-2">
    <center>
    {% include figure.html path="assets/img/projects/mti882_path_tracer/final_composition.png" title="Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}
    
    Final Image Composition
    </center>
</div>

<div class="row">
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>

            {% include figure.html path="assets/img/projects/mti882_path_tracer/homo_nomis_vs_mis.png" title="Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}
            
            Homogeneous Volumetric No MIS vs MIS
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>

            {% include figure.html path="assets/img/projects/mti882_path_tracer/homo_spectral_nomis_vs_mis.png" title="Spectral Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}

            Spectral Homogeneous No MIS vs MIS
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/mti882_path_tracer/hetero_spectral.png" title="Heterogeneous Spectral" class="img-fluid rounded z-depth-1" %}

            Heterogeneous Spectral with different parameters.
        </center>
    </div>
</div>