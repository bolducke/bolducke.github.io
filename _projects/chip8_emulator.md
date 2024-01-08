---
layout: page
title: Chip-8 - Emulator
description: Basic Emulator for the Chip-8 (Subset of Schip)
img: assets/projects/chip8_emulator/thumbnail.png
importance: 2
category: hobby
---

## Motivation

I wanted to understand a little bit more computer fundaments. Because a lot of resource are available online, I voluntarily avoided using external resources. 

## Description

This project was constructed based on specifications from the Wikipedia article on Chip-8, particularly focusing on a subset of instructions from the Schip extension.

Key aspects of the project include:

* Developed entirely from scratch.
* Implemented using OpenGL 4.6 (Glad), coupled with ImGui and SDL2 for a powerful and efficient setup.
* Features a dynamic user interface designed to visualize the emulator's internal state, enhancing user interaction and experience.

## Results

<center>
    <div class="row">
            <div class="col-12">
                <div class="row">

                <div class="col-6">
                <center>

                    {% include figure.html path="assets/projects/chip8_emulator/astrododge.gif" title="Astrododge" class="img-fluid rounded z-depth-1" %}

                </center>
            </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/projects/chip8_emulator/chipquarium.gif" title="Chipquarium" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/projects/chip8_emulator/pong.gif" title="Pong" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>

                    <div class="col-6">
                        <center>

                            {% include figure.html path="assets/projects/chip8_emulator/tetris.gif" title="Tetris" class="img-fluid rounded z-depth-1" %}
                            
                        </center>
                    </div>
                </div>
            </div>
    </div>
</center>

## Credits/Resources

[source](https://github.com/bolducke/chip8_emulator/)

[Wikipedia - CHIP-8](https://en.wikipedia.org/wiki/CHIP-8)

[Mastering Chip-8](https://github.com/mattmikolay/chip-8/wiki/Mastering-CHIP%E2%80%908)