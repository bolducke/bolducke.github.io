---
layout: page
title: PHY3075 - Numerical Modelling
description: Assignments of PHY-3075 at UdeM.
img: assets/img/projects/phy3075_numerical_modelling/thumbnail.gif
importance: 1
category: education
---

Showcase of different assignment projects done through my undergraduate study.

# Higgs Boson Detection Simplified

## Motivation

Identify the Higgs boson from sanitized data provided by CERN using a binary classifier

## Description

* Build a lightweight framework to adapt the number of layers and nodes of a neural network

## Results

* Obtain the **highest score**
* 5 layers with 13, 10, 8, 6 and 1 nodes
* Activation sigmoid function between every layer 
* 75% training and 25% test set of the original data set

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/higgs_score.png" title="Convergence based on the training/test dataset" class="img-fluid rounded z-depth-1" %}

            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/higgs_binaryclassifier.png" title="Classifier results on the unknown dataset with a score of 82.5% accuracy" class="img-fluid rounded z-depth-1" %}

            Convergence based on the training/test dataset (Top). Classifier results on the unknown dataset with a score of 82.5% accuracy (Bottom).
        </center>
</div>

# Origin of a Nuclear Accident

## Motivation

Identify the origin of a nuclear accident from gaz propagation 

## Description

* Implement a simple fluid simulation
* Build an optimization scheme

## Results

0. A domain is chosen as the region to be explored
1. Guess randomly in the region to be explored
2. Recenter around the best guess and reduce the domain by a factor
3. Stop when after a few iterations

In itself, it is a naive algorithm. However, instead of using Python, the assignment was reimplemented in Julia in parallel which makes this naive approach feasible.

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/radioactive_sim.png" title="A radioactive simulation compare to the one of reference in our textbook." class="img-fluid rounded z-depth-1" %}

            A radioactive simulation.
        </center>
        
        
        <center>

            <div class="container">
                <div class="row h-50">
                    <div class="col h-50">
                        {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/radioactive_concentration.png" title="Fitting of 3 different sensors based on the best guesses" class="img-fluid rounded z-depth-1" %}
                    </div>

                    <div class="col h-50">
                        {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/radioactive_optidivideandconquer.png" title="Vizualization of my optimization step through each sub-region" class="img-fluid rounded z-depth-1" %}
                    </div>
                </div>
            </div>

            3 different data were collected through 3 sensors based on the best parameters found through my optimization (right). A visualization of every optimization step through each sub-region (left). 
        </center>

</div>

# nu-Bootis Orbital Parametrization

## Motivation

Improve convergence of a genetic algorithm to find the best parameters of the Kepler formula to fit observed data.

## Description

* Implement a custom strategy for a genetic algorithm

## Results

Each generation is ranked through a heuristic. A portion of the generation is kept by sampling a Gaussian distribution.

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/geneticalgo_opti.gif" title="Genetic Algorithm in 2D" class="img-fluid rounded z-depth-1" %}

            Classical genetic algorithm to find the minima of a 2D sinc function.
        </center>
        
        
        <center>

            <div class="container">
                <div class="row h-50">
                    <div class="col h-50">
                        {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/geneticalgo_convergence.png" title="Genetic Algorithm Convergence Study" class="img-fluid rounded z-depth-1" %}
                    </div>

                    <div class="col h-50">
                    {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/geneticalgo_finalresult.png" title="Final Solution" class="img-fluid rounded z-depth-1" %}
                    </div>
                </div>
            </div>

            Optimization score across each iteration, comparing different optimization strategies (Left). Convergence of optimization, consistent with the Kepler formula, based on artificially sampled points. (Right).
        </center>
</div>

# Dark Matters

## Motivation

Enhance galaxy simulation by incorporating a dark matter halo to match experimental observation of gravitational potential.

## Description

* Implement a small N-Body simulation
* Estimate the gravitational potential of a simulated galaxy

## Results

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/dark_matter.gif" title="Dark Matter Contribution to Galaxy Rotation" class="img-fluid rounded z-depth-1" %}
            
            Dark matter contribution to galaxy rotation. Each blue dot represents a star. Each line in red is an isocontour of the gravitational potential.
        </center>
</div>