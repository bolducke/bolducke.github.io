---
layout: page
title: MTI882 - Path Tracing
description: Final project showcase implementing Spectral Volumetric Multiple Importance Sampling Non-Exponential Scheme (MIS NES)
img: assets/img/projects/mti882_path_tracer/thumbnail.png
importance: 2
category: formal education
---

At École des Technologies Supérieures (ETS), I had the opportunity to take an excellent course on Path Tracing by Adrien Gruson. The course provided an up-to-date overview of the current development and state-of-the-art algorithms in path tracing.

For the final project, we were asked to implement new features and compose a scene. My team chose to implement volumetric path tracing and a spectral volumetric rendering for heterogeneous media using NEE MIS based on [A null-scattering path integral formulation of light transport](https://dl.acm.org/doi/pdf/10.1145/3306346.3323025). The picture below showcases the features that I implemented with [Matthieu Beuad](https://www.linkedin.com/in/matthieu-beaud/) for our project.

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