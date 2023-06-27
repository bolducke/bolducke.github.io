---
layout: page
title: PHY3075 - Numerical Modelling
description: Assignment showcases revolving around optimization, numerical simulation, and more.
img: assets/img/projects/phy3075_numerical_modelling/thumbnail.gif
importance: 1
category: formation
---

## Higgs Boson Detection Simplified

The last project was to create a binary classifier based on sanitized data from CERN to identify if our particle was a Higgs Boson. I've implemented a small framework for a simpler NN with a way to customize the number of layers which I got the **highest score** for our binary classifier. 

I ended up with a NN with a layer of 13-10-8-6-1 with a sigmoid activation function using a ratio of 75%/25% (training/test).

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/higgs_score.png" title="Convergence based on the training/test dataset" class="img-fluid rounded z-depth-1" %}

            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/higgs_binaryclassifier.png" title="Classifier results on the unknown dataset with a score of 82.5% accuracy" class="img-fluid rounded z-depth-1" %}

            Convergence based on the training/test dataset and Classifier results on the unknown dataset with a score of 82.5% accuracy.
        </center>
</div>


## Origin of a nuclear accident

This project was to identify the origin of a nuclear accident based on data collected by the sensor. For this task, we had to implement a gas simulation and an optimization scheme from scratch.

I choose a simple brute-force strategy where I throw random guesses in a region and recenter the next guess around the best one.

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/radioactive_simcompar.png" title="A radioactive simulation compare to the one of reference in our textbook." class="img-fluid rounded z-depth-1" %}

            A radioactive simulation compare to the one of reference in our textbook.
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

            Fitting of 3 different data recolted throught 3 sensors based on the best parameters found in my optimization (right) and a vizualization of my optimization step through each sub-region. (left)
        </center>

</div>


## nu-Bootis Orbital Parametrization

The goal of this project was to improve the convergence of our genetic algorithms to find the best parameters that fit observed data given Kepler formula.

My main strategy was not to discard the worst directly but to keep some of them based on a Gaussian distribution.

<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/geneticalgo_opti.gif" title="Genetic Algorithm in 2D" class="img-fluid rounded z-depth-1" %}

            A standard genetic algorithm to find the minima of a 2D sinc function.
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

            Convergence discussion of every algorithm variation discussing the different variant benefice (Left) and Final Result of my optimization that converge to roughly the same solution (Right)
        </center>
</div>

## Dark Matters

The aim of this project was to add to the simulation of a galaxy a contribution to the gravitational potential coming from a halo of dark matter extending on the outskirts of the galaxy, sufficiently dense to “straighten” the rotation curve as expected.


<div class="row-sm mt-3 mt-md-0 pb-2">
        <center>
            {% include figure.html path="assets/img/projects/phy3075_numerical_modelling/dark_matter.gif" title="Dark Matter Contribution to Galaxy Rotation" class="img-fluid rounded z-depth-1" %}

            The scale of the simulation is done over years. Each blue dot represents a star. Each isocontour in red represents the gravitational potential. 
        </center>
</div>