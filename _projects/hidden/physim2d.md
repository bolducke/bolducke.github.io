---
layout: page
title: 2D Physic Simulation
description: Small engine for 2D simulation of classical mechanics.
img: assets/img/projects/physim2d/thumbnail.png
importance: 3
category: hidden
---

# PhySim2D

## Motivation 

Here is an old project of mine. My views have shifted a lot since then, and to be honest, I don’t think the code is great anymore. I used to get carried away with over-abstraction. Despite its flaws, I’m pretty proud of this project. It taught me a ton about myself.

## Description

* Broadphase
  * Simple Grid & Brute
* Narrowphase
  * SAT Collision Detection
  * Collision Solver [based on Erin Catto Box 2D Implementation]
* Integrators
  * Explicit Euler
  * Implicit Euler
  * Semi-Implicit Euler
  * RK4
* Constraints
  * Coherent Joint Distance between two points.
* Simple UI

### Tools
* C#
* .NET Framework

## Credits/Resources

The following blogs were uselful in my journey to learn to create a simple physic engine:

* [Ming-Lun "Allen" Chou Personal Website](https://allenchou.net/)

* [Erin Catto Talk on Physics for Games](https://www.gdcvault.com/play/1020603/Physics-for-Game-Programmers-Understanding)

The thumbnail was taken from [Wikimedia](https://en.wikipedia.org/wiki/File:Plane-Sphere_Intersection.svg).