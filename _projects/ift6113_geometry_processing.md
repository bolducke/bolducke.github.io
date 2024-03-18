---
layout: page
title: Geometry Processing
description: Assignments of IFT-6113 at UdeM
img: assets/img/projects/ift6113_geometry_processing/thumbnail.png
importance: 3
category: education
---

Showcase of assignments done in [course](http://www-labs.iro.umontreal.ca/~bmpix/teaching/6113/2021/) led by Mikkael Besselmet. The course covered the mathematical concepts and algorithms behind modern mesh processing and modeling.

# Eigen Decomposition

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
            Three lowest eigenvectors being displayed for different meshes.
        </div>
    </center>
</div>

# Shape Deformation

Implemented ["Bounded biharmonic weights for real-time deformation"](https://igl.ethz.ch/projects/bbw/bounded-biharmonic-weights-siggraph-2011-compressed-jacobson-et-al.pdf) and ["As-Rigid-As-Possible Surface Modeling"](https://igl.ethz.ch/projects/ARAP/arap_web.pdf).

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
        {% include figure.html path="assets/img/projects/ift6113_geometry_processing/arap_armadillo.png" title="ARAP Armadillo" class="img-fluid rounded z-depth-1" %}
    </center>

    <center>
            <div>
                Mesh deformation based on the red handle using an implementation of ARAP.
            </div>
    </center>
</div>

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
            {% include figure.html path="assets/img/projects/ift6113_geometry_processing/biharmonic_arap_bar.png" title="Biharmonic Arap Bar" class="img-fluid rounded z-depth-1" %}
    </center>

    <center>
        <div>
            Mesh deformation of a bar using biharmonic (Right) and ARAP (Left).
        </div>
    </center>
</div>

# Solving Heat Equation on Manifold

ImplementedS ["The Heat Method for distance computation"](https://www.cs.cmu.edu/~kmcrane/Projects/HeatMethod/).

<div class="col-sm mt-3 mt-md-0 pb-2">
    <center>
    {% include figure.html path="assets/img/projects/ift6113_geometry_processing/heat_evolution_bunny.png" title="Heat Evolution on a Bunny" class="img-fluid rounded z-depth-1" %}
    </center>
    <center>
        <div>
            Random initiliaziation of heat. Then, vizualisation of different step through the propagation of heat on the manifold.
        </div>
    </center>
</div>


# Shape Fairing

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
