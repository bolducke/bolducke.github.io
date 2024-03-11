---
layout: page
title: Path Tracing
description: Final assignment of MTI-882 at ÉTS.
img: assets/img/projects/mti882_path_tracer/thumbnail.png
importance: 2
category: education
---

## Motivation

At École des Technologies Supérieures (ETS), I had the opportunity to take an excellent course on Path Tracing by Adrien Gruson. The course provided an up-to-date overview of the current development and state-of-the-art algorithms in path tracing. The result (in french) of the competition are available here at [ÉTS - Rendering Competition 2022](https://profs.etsmtl.ca/agruson/competition/2022/)


## Description

### Requirements

* Add new features to our rendering engine
* Compose a scene from the ground up 

## Results

### Majors Features

* Implemented a volumetric path tracing
* Implemented a spectral volumetric rendering for heterogeneous media using NEE MIS based on [A null-scattering path integral formulation of light transport](https://dl.acm.org/doi/pdf/10.1145/3306346.3323025)

### Gallery

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
            
            Homogeneous volumetric with no MIS (left) and MIS (right)
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>

            {% include figure.html path="assets/img/projects/mti882_path_tracer/homo_spectral_nomis_vs_mis.png" title="Spectral Homogeneous No MIS vs MIS" class="img-fluid rounded z-depth-1" %}

            Spectral homogeneous with no MIS (left) and MIS (right)
        </center>
    </div>
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/mti882_path_tracer/hetero_spectral.png" title="Heterogeneous Spectral" class="img-fluid rounded z-depth-1" %}

            Heterogeneous Spectral with different parameters.
        </center>
    </div>
</div>

## Credits/Resources

Team:
* [Karl-Étienne Bolduc](bolducke.github.io)
* [Matthieu Beuad](https://www.linkedin.com/in/matthieu-beaud/)