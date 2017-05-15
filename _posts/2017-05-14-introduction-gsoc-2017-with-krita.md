---
layout: post
title: Introduction for GSoC 2017 with Krita
color: blue
subtitle: Develop a showcase of Krita's new scripting support
bigimg: /img/krita.png
tags: ['KDE','GSoC','Krita']
---

Hi Everyone, is everything ok? I hope so.

I'm here again and I will talk about my accepted GSoC proposal, but how every history, I have to start from the start, so sit down, drink a coffee or a hot chocolate(I like) and have fun.

I'm from Brazil, to be more specific from Salvador, Bahia. I'm an undergraduate student in Analysis and System Development. I'm not like so many other people that code since their 9 years old or something like that. I just wrote my first line of code with 20 years old and now I have 23, but like my mother says, "It's never late to do something, no matter what" (Yeah, my mother is amazing. By the way, Happy Mother's Day). 

In first years in the college, I had the opportunity to work in a software house, that works with proprietary software. I didn't like that experience for so many reasons, but I was holding myself for money (I'm poor). Someday a teacher from my college invite to a course about Qt and C++ and told to us that we can choose what we want to do and presented KDE and Open Source. I quit my job and started to go to the college in my free time. In this time I studied python and read some books about that and I loved it. 

I worked in a one-year project with python in the college and someday that same professor told me about Season of KDE 2016-2017. We take a look at the GSoC Ideas from 2016 and I found Python Scripting for Krita, I thought: "That's for me". I talked with Boudewijn Rempt and I wrote a proposal to the SoK for work in a GUI in PyQt to execute and save python scripts in the Krita (Scripter) that access the python API exposed through likis. After 4 months of work I ended up the SoK with success, you can see the GUI working bellow.

<div style="vertical-align:middle; text-align:center">        
    <img src="/img/scripter_krita.png">
     <figcaption><i>Interactive GUI to execute python code inside Krita.</i></figcaption>
</div>


After all the history, I can introduce you to my GSoC proposal for this year...

![GSOC](/img/GSoC-logo-horizontal.svg)


My work in the GSoC is a continuation from my SoK's work. I have to implement scripts to be executed in the Scripter and plugins to be added to the Krita GUI. A really important part of my work is to talk with more users to set a good group of scripts and plugins to be implemented during this period and define how my work will be available to the users. You can read the proposal's abstract bellow


> Krita is a professional free and open source painting program. The Krita's tools and features are focused on digital painting, concept art, illustration and texturing.
>
> Some steps of working in software for digital painting can be repetitive and consequently boring, like exporting a painting, configuration of the document's properties, applying filters and a set of other tasks. An approach to solve this problem can be to make it scriptable. Making a software scriptable is expose an API for the users and offer some way to execute your own code.
>
>Python is the Krita's script language and the standard language in the VFX industry, but we are talking about artists that in your majority don't code. My proposal is focused in solve this problem working together with the Krita's community to implement a set of scripts and plugins in python, to attending your needs about this repetitive and boring tasks.


You can read my full proposal [here](https://eliakincosta.github.io/files/Eliakin-GSoCproposalforKrita.pdf).

That's it for now, I'm really excited to code and to help Krita community. Until next week, See ya!!
