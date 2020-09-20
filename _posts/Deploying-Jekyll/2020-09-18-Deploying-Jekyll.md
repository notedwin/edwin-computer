---
title: Deploying Jekyll using Nginx and Jenkins.
date: 2020-09-18 10:00:00 +07:00
tags: [DevOps]
description: Messing around with DevOps production. 
---

Old Website
---------------------
For my old website, I used [Gatsby](https://www.gatsbyjs.com), which was easy to deploy thanks to [vercel](https://vercel.com).  
Vercel took every commit I published for my website repository and magically created a production website.  

New Website
------------------------------------------------------
I changed to Jekyll from GatsbyJS, as there was alot of overhead in making that website.  
I know making a website should not be breeze but I also thought why am I making a complex website for a blog.
I don't have 1,000,000 hits a day nor do I have some sort of web store.
Ya feel me?
Anyways, Jekyll >= Gatsby for now.

Nginx and Jenkins
---------------------------------
What is [nginx](https://www.nginx.com)?
-------------------------------------
According to Nginx, Nginx Open Source is "software for web serving reverse proxing, caching, load balancing, media streaming, and more." 

I primarily use Nginx as a web server for this [website](https://edwin.computer). It just listens to traffic from specific ports and redirects that traffic to the appropriate location.

What is [Jenkins](https://www.jenkins.com)?
-----------------------------
From the Jenkin's website, "The leading open source automation server, Jenkins provides hundreds of plugins to support building, deploying and automating any project."

I primarily use Jenkins to automate the process of deploying my website to my Nginx Server. Using Jenkin, I can automate pulling my websites github repository and building the website when there is a new commit, reporting the build status back to github. That's pretty cool. 

Difficulties
------------------------------
Nginx has great documentation. I was able to set up https with an SSL certificate from [CertBot](https://certbot.eff.org/). The process was simple. 
Jenkins gave me much difficulties as the user interface is not very beginner friendly. At first, I couldn't get my project to even build. Once i got over the first struggles, it made alot of sense why things are laid out as such.

Conclusion
------------------------------

