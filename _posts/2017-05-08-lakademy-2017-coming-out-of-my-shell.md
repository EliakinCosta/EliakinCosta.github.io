---
layout: post
title: LaKademy 2017
color: blue
subtitle: Coming out of my shell.
bigimg: /img/group_photo.jpg
tags: ['KDE','LaKademy 2017','Krita']
---

Hi Everyone, is everything ok? I hope so. ^-^

I'm here for the first time to talk about my first participation in a sprint event and try to keep coming out of my shell. To clarify this, I have to back in time...

![Meme Images](/img/winter-is-coming-brace-yourself-a-long-text-is-coming.jpg)

I've aways been an introspective person and when I was approved to Analysis and Systems Development Course, I thought that I don't would need to talk with people anymore (while working at least) and I was happy with this xD. Things were going well, until the day that I met the open source concepts and KDE, through my professor, Sandro Andrade (yes, it's your fault :p). It was love at first sight, I liked the idea to share knowledge and help another people or I was just thinking that I could work with my shorts, I hate pants. I will never know the truth xD.

Sandro told me sometimes that KDE is not about software is about people, I didn't understand your message that day. In the last year, I was approved to Season of KDE and the main problem to me besides code was integrate me the community. My mentor Boudewijn, helped me a lot at this point and today he is an inspiration to me. Thanks, Boud.

Now you understand what is my shell, but we will jump this part and go to the LaKademy...

My first day in the LaKademy started with each one presenting yourself, something like an "about me" session. It was amazing because there were so many different persons, that contribute from different ways, from different points of the Brazil. After this initial moment, we start to work in our KDE projects, in my case, I would keep my work in the Krita. 

My work in the LaKademy was basically:


* First day
    * I talked with Boud about implement some tests to Python Scripting API and he approved my suggestion.
    * I chat with Dmitry Karzakov to understand the structure of the current tests in the Krita.
    * I wrote a basic structure with a unitest.TestCase simple subclass in python.
    * I studied how to integrate python unit tests with cmake test.
    * My initial attempts did not succeed, so I needed some help.
    * I talked with Dmitry again and he gave me a good idea to integrate this test, but that would a work to the next day.

* Second day
    * Integration of the python unit test with cmake was well succeeded. Thanks, Dmitry. :)
    * I did a resume of all classes that don't need a GUI to work


<div style="vertical-align:middle; text-align:center">        
    <img src="/img/cmake_test_python.png">
     <figcaption><i>Running tests integration with success.</i></figcaption>
</div>

* Third day
    * It was removed all unnecessary literal strings in the cmake file
    * I created a directory structure to tests inside pykrita directory
    * Tests running with success
    * Branch created and pushed was made
    * Review was sent to the phabricator(https://phabricator.kde.org/D5675).

<div style="vertical-align:middle; text-align:center">        
  <img src="/img/push_in_my_branch.png" width="600">
  <figcaption><i>Code pushed to remote repository.</i></figcaption>
</div>

* Fourth day
    * Meg - framework to development Qt mobile applications:  plugins architecture refactoring

<div style="vertical-align:middle; text-align:center">        
  <img src="/img/me_and_sandro.jpg" width="600">
  <figcaption><i>I and Sandro working on Meg.</i></figcaption>
</div>

Yeah, time really goes fast and the LaKademy 2017 is over, but I'm happy to meet the people behind the computers and be closer to the community. Until the next week, GSoC is waiting for me. See ya!!
