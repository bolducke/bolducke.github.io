---
layout: page
title: Gaussian Splatting Renderer 
description: Gaussian Splatting Renderer for Desktop and Web.
img: assets/projects/wasm_splatrenderer/thumbnail.png
importance: 1
category: hobby
---


## Motivation

The recent publication of '3D Gaussian Splatting for Real-Time Radiated Field Rendering' has led to the introduction of Gaussian splatting as an intriguing alternative to neural field due to its practicality to reconstruct 3D scene.

Based on recent interest in the method, I was curious to learn more about how they can render scene effectively. In the end, I came up with a simple OpenGL program to visualize 3D Gaussian.

## Description

This project is based on articles available onlines and papers mentioned in the resource section. The renderer is implemented using a splatting technique inspired from "EWA Splatting". 

A 3D scene is given to the program as a set of Gaussian that are encoded similarly to the original paper. Then, an image is produced by accumulating them onto a screen using alpha blending. To produce a realistic image, gaussian are, then, sorted relative to the "z" axis of the camera. Each gaussian position and covariance are transformed in the NDC space. 

To make it run faster, a small bounding-box is render around the gaussian splat to reduce the number of call in the fragment shader. 

* Support original `.ply` format to load a scene.
* Extend "EWA Splatting" for any projective transformation.
* Display content using **SDL**, **OpenGL 3.0 ES** for Desktop and **Webgl** for Web.
* Support web through **Emscripten** and **WASM**.

## Known Limitation

* Parsing directly from `.ply` is slow.
* Multithreading sort is slow on web even with `-pThreads`.
* Camera inputs are janky and non-intuitive.

## Results

<center>
    <div class="row">
            <div class="col-12">
                <div class="row">

                <div class="col-12">
                <center>

                    {% include video.html path="assets/projects/wasm_splatrenderer/desktop_showcase_legoset.webm" title="Hangman" loop=1 autoplay=1 muted=1 class="embed-responsive z-depth-1" %}

                </center>
                </div>
                </div>
            </div>

            <div class="col-12">
                <div class="row">

                <div class="col-12">
                <center>

                    {% include video.html path="assets/projects/wasm_splatrenderer/web_showcase_legoset.webm" title="Hangman" loop=1 autoplay=1 muted=1 class="embed-responsive z-depth-1" %}

                </center>
                </div>
                </div>
            </div>
    </div>
</center>

## Credits

"lego_bouquet.ply" is originally part of a scene provided by "3D Gaussian Splatting for Real-Time Radiance Field Rendering". The content has been edited to only display the lego set.

## Resources

[source](https://github.com/bolducke/wasm_splatrenderer)

[EWA Splatting](https://ieeexplore.ieee.org/abstract/document/1021576?casa_token=EJ5oFxpJxBoAAAAA:Z9OyQ8892KNMgyUu9k0cqa8O3Bj75nsyum3g-_8Uhq7a_sCI25yJSj0DOGZk6Y89aGDRMehknng)

[3D Gaussian Splatting for Real-Time Radiance Field Rendering
](https://arxiv.org/abs/2308.04079)


[Super Splat (for editing scene)](https://playcanvas.com/supersplat/editor)