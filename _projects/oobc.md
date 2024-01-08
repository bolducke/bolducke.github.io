---
layout: page
title: OOBC
description: Overengineer/Overthink breakout clone
img: assets/img/projects/oobc/thumbnail.png
importance: 2
category: hobby
---

# Overengineer/Overthink Breakout Clone

<center>
{% include figure.html path="assets/img/projects/oobc/game.png" title="In Renovation Home" class="img-fluid rounded z-depth-1 center" %}
</center>

## Motivation

As a hobby and with a desire to learn and explore programming design, I developed a small Breakout game using Odin (C-like Language) and SDL in my free time. I intentionally over-engineered the project to more easily detect the pain points of my design.

My goal was to create a flexible product that is easy to refactor and add features to while not compromising too much on performance by using a cache-friendly approach. However, because I was more interested in modularity, I didn’t focus much on performance. I deliberately avoided OOP to explore alternative modes of thought.

## Description

* ECS-like Architecture without any framework
* Hierarchy (Tree-Like) Relation between Entity
* True Separation between Geometry Intersection Algorithm and Physics Computation
    * Geometric Algorithm to Detect Collision, Intersection, and Compute Centroid for a small set of "Geometry".
    * "Advanced" Physic Sim (Based on my old Physic Engine)
        * Multiples Integrators: RK4, Explicit Euler, Semi-Implicit Euler
        * Contact Resolution in two steps: Position-Based Solver & Velocity-Based Solver *(Inspired of Box2D)*
* Text/Font support
* Affine Transform Matrix

## Credits/Resources

[source](https://github.com/bolducke/OOBC)

The contact resolution solver was inspired by [Box2D](https://box2d.org/) works.