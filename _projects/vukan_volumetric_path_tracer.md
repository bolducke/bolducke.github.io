---
layout: page
title: GPU Path Tracing
description: Spectral Volumetric Path Tracing using Vulkan
img: assets/img/projects/vukan_volumetric_path_tracer/thumbnail.png
importance: 1
category: hobby
---

To learn Vulkan (a second time), I followed a recommendation about this [resource](https://nvpro-samples.github.io/vk_mini_path_tracer/index.html) online to better understand how vulkan is working behind the scene. 


## Briefly
* Loaded custom extensions like **VK_KHR_ray_query** and **VK_KHR_acceleration_structure**
* Allocated buffers to be used in our shader
* Loaded a custom model
* Used **BLAS** and **TLAS** for our custom model
* Created a compute pipeline 
* Synchronized properly the pipeline and submit it through the command buffer using a pipeline barier.
* Wrote back the data in a file

## Contribution
* Created a **blender** scene with a way to **add custom attributes** and **save them** into a '.npy'.
* Added a way to **load material** information to the shader stage.
* Added different **materials** such as light, glossy reflection and more.
* Implemented a **volumetric** path tracer based on my previous course using 
    * **Free-path Sampling**
    * **Henyey-Greenstein Phase Function**
    * **Spectral Sampling**

With 2056 samples and a depth of 32, I was able to render the volumetric path tracing in **less than 1 seconds** using a RTX 4070 Laptop.

## Gallerie

<center>
    <div class="row">
            <div class="col-12">
                <center>

                    {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/path_tracing.jpg" title="Path Tracing on GPU" class="img-fluid rounded z-depth-1" %}

                    Path Tracing using differents materials.

                </center>
            </div>

            <div class="col-12">
                <div class="row">

                    <div class="col-12">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_green.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                            Volumetric Path Tracing using Free-Flight Sampling.
                        </center>
                    </div>

                    <div class="col-12">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_yellow.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                            Volumetric Path Tracing using Free-Flight Sampling.
                        </center>
                    </div>

                    <div class="col-12">
                        <center>

                            {% include figure.html path="assets/img/projects/vukan_volumetric_path_tracer/volumetric_blue.png" title="Volumetric" class="img-fluid rounded z-depth-1" %}
                            
                            Volumetric Path Tracing using Free-Flight Sampling.
                        </center>
                    </div>
                </div>
            </div>
    </div>
</center>