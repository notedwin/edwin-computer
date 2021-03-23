---
title: projects
permalink: /projects/
layout: page
excerpt: random projects
comments: false
---

## Cyberattack Map

<div class="embed-responsive">
<embed src="https://map.edwin.computer">
</div>
[Github repository](https://github.com/notedwin/attack-map)

I wanted to generate a world map that showed all the people who were trying to break into my raspberry pi that hosts this website.

This project took many iterations due to complications but I have a working product now.

[Blog Post for Cyber Attack Map](https://edwin.computer/attack-map/)

## Online Grocery Store

Project for my database organization class.  
[Github Repository](https://github.com/notedwin/GroceryStore)

## Online Restaurant Application

<div class="embed-responsive">
<embed src="https://restaurant.edwin.computer">
</div>
Project for my software engineering class.  
[Live website](https://restaurant.edwin.computer)  
[Github Repository](http://github.com/notedwin/restaurant-app)

This repository serves as my catch all: ["Interview Practice"](https://github.com/notedwin/interview-practice)

I work with different api, modules, websites. I solve problems from project euler, leetcode, or just some daily dilemma that I can solve with programming.

## Old website

[Github Repository](https://github.com/notedwin/personal-website)

My gaudy website. I'll make sure to host it for historical purposes.

{% for image in site.static_files %}
{% if image.path contains 'images/slider' %}
<img src="{{ site.baseurl }}{{ image.path }}" alt="image" />
{% endif %}
{% endfor %}
