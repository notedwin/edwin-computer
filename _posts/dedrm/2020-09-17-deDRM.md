---
title: Remove DRM from PDF.
date: 2020-10-30 10:00:00 +07:00
tags:
description: DeDRM
---

## What the heck is DRM?

Digital right management is a systematic approach to copyright protection for digital media.

## Why are you removing it?

The dilemma I was in was that one of my classes required a book from independent publisher.

Said independent publisher sold PDF version of the book for cheaper than the hard cover book.

I clutched my pearls and decided to go for the cheaper book. I saved like 15 dollars.

Now here comes the problem, I did not have adobe digital editions on my Laptop since I was running Linux and Linux is notorious for not supporting adobe applications nicely.

Nor did I want to figure out how to run a janky version of digital editions.

So as any reasonable person would do, I asked my girlfriend to use her Mac to use Adobe digital editions.

I did not know that the DRM on this book limited to one device.

I can't ask my girlfriend to borrow her laptop every time I want to read this book.

## Removing the DRM

Googling "Remove DRM from a book" is not a crime, but the publisher probably is not too happy about this.

After a couple refined searches, I luckily found a tool to remove DRM from books called DeDRM.

The tool uses Python2 and relies on Adobe digital editions 2.0.

So you have to install some old software.

Using the adobe digital editions file (.ACSM), run a python file on the .ascm file to genrate the adobe keys. Then it decrypts the ascm file into a pdf using the library.

By this poor explanation, you can see that I am not an expert but I think this should be an option you should and can consider.

[dedrm](https://github.com/apprenticeharper/DeDRM_tools)
