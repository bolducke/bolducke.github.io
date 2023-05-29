---
layout: page
title: OOBC
description: Overengineer/Overthink breakout clone
img: assets/img/projects/oobc/game.png
importance: 1
category: hobby
---

{% include figure.html path="assets/img/projects/oobc/game.png" title="In Renovation Home" class="img-fluid rounded z-depth-1 center" %}


[source_code](https://github.com/bolducke/exploration_odin-architecture/tree/master)

# Overengineer/Overthink Breakout Clone

## Motivation

As a hobby and a desire to learn and explore programming design, I coded a small Breakout Game *as an excuse* using Odin (C-Like Language) and SDL in my free time. I intentionnaly overenginner/overthink the project to detect more easily the pain point of my design.

My intent was to create a product where it's flexible (easy to refactor and to add features) while not compromising too much on performance (using cache friendly approach). However, because I was more interested in the overall architecture, I didn't focus a lot on performance. I intented to stay away from OOP to experiment different way of "thinking".

You can see a breakdown on the design at [blog]({% post_url 2023-05-28-design_takeaway_ecsarchetype %})

## Main Features

* ECS-like Architecture without any framework
* Hierarchy (Tree-Like) Relation between Entity
* True Separation between Geometry Intersection Algorithm and Physics Computation
    * Geometric Algorithm to Detect Collision, Intersection, Compute Centroid for a small set of "Geometry".
    * "Advanced" Physic Sim (Based on my old Physic Engine)
        * Multiples Integrators: RK4, Explicit Euler, Semi-Implicit Euler
        * Contact Resolution in two steps: Position Based Solver & Velocity Based Solver *(Inspired of Box2D)*
* Text/Font support
* Affine Transform Matrix