---
layout: page
title: IFT6113 - Geometry Processing
description: Assignment showcase featuring Discrete Operators, Fairing, and Deformations.
img: assets/img/projects/ift6113_geometry_processing/thumbnail.png
importance: 3
category: formation
---

During my time at Udem, I had the opportunity to participate in a [course](http://www-labs.iro.umontreal.ca/~bmpix/teaching/6113/2021/) led by Mikkael Besselmet that introduced us to geometry processing. The course covered the mathematical concepts and algorithms behind modern mesh processing and modeling.

Here is a brief overview of some of the algorithms we implemented during the course.

### Eigen Decomposition

<div class="col-sm mt-3 mt-md-0 pb-2">
    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/ift6113_geometry_processing/eigendecomposition_bunny.png" title="Eigenvalues" class="img-fluid rounded z-depth-1" %}
        </center>
    </div>

    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/ift6113_geometry_processing/eigendecomposition_camel.png" title="Eigenvalues" class="img-fluid rounded z-depth-1" %}
        </center>
    </div>

    <div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/ift6113_geometry_processing/eigendecomposition_lowpolycamel.png" title="Eigenvalues" class="img-fluid rounded z-depth-1" %}
        </center>
    </div>

    <center>
        <div>
            Three lowest eigenvectors being displayed for different meshes
        </div>
    </center>
</div>

### Deformation

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
        {% include figure.html path="assets/img/projects/ift6113_geometry_processing/arap_armadillo.png" title="ARAP Armadillo" class="img-fluid rounded z-depth-1" %}
    </center>

    <center>
            <div>
                Mesh deformation based on the red handle using a custom implementation of ARAP.
            </div>
    </center>
</div>

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
            {% include figure.html path="assets/img/projects/ift6113_geometry_processing/biharmonic_arap_bar.png" title="Biharmonic Arap Bar" class="img-fluid rounded z-depth-1" %}
    </center>

    <center>
        <div>
            Mesh deformation of a Bar using Biharmonic (On the right) and ARAP (On the Left)
        </div>
    </center>
</div>

### Solving Heat Equation on Manifold

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
    {% include figure.html path="assets/img/projects/ift6113_geometry_processing/heat_evolution_bunny.png" title="Heat Evolution on a Bunny" class="img-fluid rounded z-depth-1" %}
    </center>
    <center>
        <div>
            Random initiliaziation of heat. Then, vizualisation of different step through the heat propagation on the manifold.
        </div>
    </center>
</div>


### Fairing

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
    <div class="col-sm mt-3 mt-md-0 pb-2">
        {% include figure.html path="assets/img/projects/ift6113_geometry_processing/fairing_bunny.png" title="Bunny Fairing" class="img-fluid rounded z-depth-1" %}
    </div>
    </center>

    <center>
        <div>
            Fairing high frequency eigen value of a mesh.
        </div>
    </center>
</div>
