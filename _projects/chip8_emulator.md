---
layout: page
title: Chip-8 - Emulator
description: Basic Emulator for the Chip-8 (Subset of Schip)
img: assets/projects/chip8_emulator/thumbnail.png
importance: 2
category: hobby
---

[Source Code](https://github.com/bolducke/chip8_emulator/)

## Motivation

* Educative Purpose (Avoided resource outside of the one described below)
* Familiarize myself with basic computer fundamentals
* Generate nice looking gif

## Description

The project relied on the specifications outlined in the Wikipedia article, which encompassed a subset of instructions derived from the Schip for Chip-8.

* From Scratch.
* Implementation is done using OpenGL 4.6 (Glad) + ImGui + SDL2.
* Dynamic UI to visualize the inner state of my emulator.

## Gallery

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

## Resource

[Wikipedia - CHIP-8](https://en.wikipedia.org/wiki/CHIP-8)

[Mastering Chip-8](https://github.com/mattmikolay/chip-8/wiki/Mastering-CHIP%E2%80%908)