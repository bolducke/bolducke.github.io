---
layout: page
title: IDCards Generators
description: Small script to generate IDCards and print them.
img: assets/img/projects/idcards_generators/thumbnail.png
importance: 2
category: freelance
---

{% include figure.html path="https://user-images.githubusercontent.com/26026137/233532015-bd9e0607-3aa1-4786-99a0-5040b3a5d350.png" title="In Renovation Home" class="img-fluid rounded z-depth-1" %}

## Motivation

For FoieGraph 2022, I needed to create ID cards for every member attending the event. Unfortunately, I couldn’t find any script for this task without paying a fee. Instead, I made a small script to create simple ID cards. I am making the source available if it can help others.


## How does it work?

The formatting of every card is handled using `html` and `css`. The script in Python is used to generate the documents holding the ID.

1. You create an `html` template for your ID Card. (Adobe Illustrator, etc).
2. You need to specify an id on the field where you need to insert information.
3. You run the script. (You only need to alter directly the 3-4 variables)
4. You print the document with your browser. (`ctl-p` on Chrome)

In the template (`template/page.html`), you can fine-tuned the margin to cut through and keep the content intact while printing. Most printers have a “dead zone” where the content is not properly drawn.

## Credits/Ressources

The design on the ID Card was done by Mariia Myronova. 

[source](https://github.com/bolducke/idcards_generator)