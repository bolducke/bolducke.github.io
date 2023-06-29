---
layout: page
title: Websites
description: Websites designs & creations
img: assets/img/projects/websites/thumbnail.png
importance: 1
category: freelance
---

In the summer of 2020, while I was a second-year student at university, I wanted to experiment web technologies because I didn't have the chance to explore them before. I throw myself at the most common framework such as laravel, django, vuejs and firebase. Over 2020, I produce two websites.

## [In Renovation I.N inc](https://inrenovation.com/) (Summer 2020)

[source code](https://github.com/bolducke/website_inrenovationinc)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/inrenovation_home.png" title="In Renovation Home" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/inrenovation_gallery.png" title="In Renovation Gallery" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/inrenovation_contact.png" title="In Renovation Contact" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Motivation

I made contact with a contractor who needed to rework his website. After we discuss the requirements, I rapidly started to use the tool that I learned over the summer. I was responsible for the overall conception.

### Overall Requirements
* Look Modern & Professional
* Custom Domain Name with a personalized email 
* Can alter the gallery easily with new pictures

### Tools/Services Used
* Vue 2
* Vuetify 2
* Firebase
* NameCheap Domain Name + Personalize Email Account with Domain Name

### Major Designs Decision

1. I customized most of the components of Vuetify 2 to give them a personalized look.
2. I separated each section on the page into its own components to reduce repetition and make it simpler to maintain.
3. I enabled the client to access Firebase storage directly to upload their own picture and make amendments if needed. To reduce bandwidth, I also created a small script to reduce the picture size uploaded and to create thumbnails.
4. I chose Namecheap for the domain name and for the service letting me personalize the email with a custom domain name. This makes the website look more professional. Then, I redirected every message to their own personal email account.

## Lan "Quart de Nuit" [Draft] (Spring 2020)

[source code](https://github.com/lan-pascal)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/qdn_home.png" title="In Renovation Home" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/qdn_competition.png" title="In Renovation Gallery" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/websites/qdn_boardgame.png" title="In Renovation Contact" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Before the pandemic, I helped organize small events with great friends where people would play together on different types of games from the evening through the morning. We named the event “Quart de Nuit” [Night Shift]. We held 3-4 events at a Gaming Cafe and were able to regroup 30 people. Then, we decided to go bigger and loan a room. We tried to have a karaoke, a screen with the competition, local gaming stands to play together, some gaming board games, and a bar. We decided that we needed a website so that it would be simpler to be paid. Unfortunately, the pandemic happened and we had to cancel everything.

I was responsible for the overall backend/frontend communication with the API.

### Overall Requirements
* Countdown
* Login Account
* Ticketing
* Interesting Looking Website

### Tools/Services Used
* Vue 2
* Vuetify 2
* Laravel
* Stripe
* NameCheap Domain Name

### Major Designs Decision

1. Stripe was a great platform to integrate with our service to let users pay for the ticket. We wanted to reduce as much as fee as possible and stripe was a great option in that regard.
2. Laravel was meant to be the backend to handle the login and processing to let users pay in security.
3. Vue & Vuetify was meant to be used as the foundation for the website for ease to learn.