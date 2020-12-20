---
title: projects
permalink: /projects/
layout: page
excerpt: random projects
comments: false
---
Personal project that did not end up working out  
[attack map](https://github.com/notedwin/attack-map)  

This project had to many complications. I wanted to use rsyslog but I was having a hard time getting it to run. Everything is outlined in this blog post. 


Another personal project is "Interview practice", It is only called that because I have not had time to clean out the directory. If it aint broke don't fix it.  
["Interview Practice"](https://github.com/notedwin/interview-practice)  

I work with different api, modules, websites. I solve problems from project euler, leetcode, or just some daily dilemmna that I can solve with programming.

Project for my database organization class.  
[grocery-store repo](https://github.com/notedwin/GroceryStore)  

Project for my software engineering class.  
[restaurant live](https://restaurant.edwin.computer)  
[restaurant repo](http://github.com/notedwin/restaurant-app)


My gaudy website. I'll make sure to host it for historical purposes.  

[old website](https://github.com/notedwin/personal-website)  
My blog posts outline a focus on infastructure. I have a raspberry pi running Nginx to show my webpages and Jenkins to automate building the websites from github.  

My projects have a focus  


{% for image in site.static_files %}
    {% if image.path contains 'images/slider' %}
        <img src="{{ site.baseurl }}{{ image.path }}" alt="image" />
    {% endif %}
{% endfor %}