---
layout: page
title: GPU Path Tracing
description: Spectral volumetric path tracing using Vulkan
img: assets/img/projects/vukan_volumetric_path_tracer/thumbnail.png
importance: 1
category: hobby
---

# Vulkan Volumetric Path Tracer

## Motivation

From an online recommendation, I recently discovered a fantastic Vulkan resource for beginners [vk_mini_path_tracer](https://nvpro-samples.github.io/vk_mini_path_tracer/index.html). It stands out for its clear explanations and user-friendly approach. Highly recommended for anyone diving into Vulkan.

## Description

* Load custom extensions like **VK_KHR_ray_query** and **VK_KHR_acceleration_structure**
* Allocate buffers to be used in a shader
* Load a custom model
* Use **BLAS** and **TLAS** for a custom model
* Create a compute pipeline 
* Synchronize properly the pipeline and submit it through the command buffer using a pipeline barrier.
* Write back the data in a file

## Results

With 2056 samples and a maximum bounce rate of 32, I render the images in the gallery in **less than 1 second** using an RTX 4070 Laptop.

### Contributions

* Create a **blender** scene with a way to add custom attributes and save them into a '.npy'.
* Add a way to load material information to the shader stage.
* Add **different materials** such as light, glossy reflection, and more.
* Implement a **volumetric path tracer** based on a previous course using 
    * **Free-path Sampling**
    * **Henyey-Greenstein Phase Function**
    * **Spectral Sampling**

### Gallery

<center>
    <div class="row">
            <div class="col-12">
                <div class="row">

                <div class="col-6">
                <center>

                    {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/path_tracing.jpg" title="Path Tracing on GPU" class="img-fluid rounded z-depth-1" %}

                </center>
            </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_green.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_yellow.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_blue.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>
                </div>
            </div>
    </div>
</center>

## Credits/Resources

[source](https://github.com/bolducke/vk_volumetric_path_tracer)

[vk_mini_path_tracer](https://nvpro-samples.github.io/vk_mini_path_tracer/index.html)