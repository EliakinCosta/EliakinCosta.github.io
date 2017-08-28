---
layout: post
title: GSoC - Final Period
color: blue
subtitle: Experience beyond the code
tags: ['KDE','GSoC','Krita']
date: 2017-08-28 00:20:00
---

Hi everyone, how is it going? Fine, I hope.

<p style="text-align: justify;">Today, I will talk about my work in the Krita during the month 2-3 of the coding period. Yeah, it's over :(. </p>


## Overview

<p style="text-align: justify;">I implemented some scripts to the showcase and some new plugins as well. You can find my task <a href="https://phabricator.kde.org/T5885">here</a> and see more details about my progress during GSoC. In a nutshell, I implemented the follow scripts/plugins:</p>

- Simple scripts defined previously in the task
- Plugin to export all the layers (batch)
- Document Tools Plugin
- Fix and Improve Ten Brushes Plugin
- Last Documents Thumbnails Docker
- Implement Ten Scripts Plugin

### Simple Scripts

<h6>Export, Duplicate Image and Export Layers</h6>

<b>Export and Duplicate Scripts</b>

<p style="text-align: justify;">First, I had to write scripts to automatize some simple tasks like export and duplicate image. They are simple, but very common when manipulating documents in the Krita. You can see the implementation below and a simple use case on <b>main</b> function after.</p>

<figure>
  <img src="{{site.url}}/img/simple_scripts_implementation.png"/>
  <figcaption style="text-align:center;">Functions to export and duplicate image.</figcaption>
</figure>
<p></p>
<figure>
  <img src="{{site.url}}/img/simple_scripts_example.png"/>
  <figcaption style="text-align:center;">Simple use case to export and duplicate scripts.</figcaption>
</figure>

<b>Script to export all layers</b>

<p style="text-align: justify;">One of the scripts suggested from the community was the <a href="http://registry.gimp.org/node/28268">"Export All Layers"</a>. That script was suggested from some users of the GIMP and with the current API, We could provide that implementation. You can see the recursive export function below, but you can find the complete implementation on the Phabricator <a href="https://phabricator.kde.org/T5885">task</a>.</p>

<figure>
  <img src="{{site.url}}/img/export_all_layers_script.png"/>
  <figcaption style="text-align:center;">Recursive function that exports all sub-layers with a predefined configuration.</figcaption>
</figure>

### Plugin to export all the layers (batch)

<b>GUI Mockup</b>

<p style="text-align: justify;">The GUI Mockup was the screenshot of the GIMP's plugin. The main idea here was to make a GUI with the main options available on GIMP with the currently available API. This image that follows is the gimp plugin.</p>

![GSOC](/img/gimp_export_all_layers.png)

<b>GUI implementation with PyQt</b>

<p style="text-align: justify;">You can see below the final result of my work. That's a more simple GUI with just some option that can be extended in the future, though.</p>

![GSOC](/img/krita_export_all_layers.png)

<b>Testing</b>

<p style="text-align: justify;">Below, you can see the result of the export to the selected directory. You can compare with the previously selected configuration.</p>

![GSOC](/img/krita_export_result_1.png)

![GSOC](/img/krita_export_result_2.png)


### Document Tools Plugin

<b>GUI Mockup</b>

<p style="text-align: justify;">The main idea here was to have a <a href="http://doc.qt.io/qt-5/qtabwidget.html">QTabWidget</a> that you can easily extend adding new tools like tabs. It's similar to the <a href="https://phabricator.kde.org/T4551">Scripter</a> plugin that's showed below. </p>

![GSOC](/img/scripter_krita.png)

<b>GUI implementation with PyQt</b>

<p style="text-align: justify;">You can see below the final result of my work. That's a simple GUI with extensible code to future implementations. We have Canvas Size, Scale and Rotate option at the moment.</p>

![GSOC](/img/krita_document_tools_plugin.png)

<b>Testing</b>

<p style="text-align: justify;">Below, you can see the result of the rotate applied to one document, but you can apply to multiple documents as well.</p>

Before                                     |  After
:-----------------------------------------:|:-----------------------------------------:
![GSOC](/img/before_rotate_action.png)|![GSOC](/img/after_rotate_action.png)

### Fix and Improve Ten Brushes Plugin

<b>Concept</b>

<p style="text-align: justify;">The Ten Brushes Plugin is a GUI where you can assign brushes to shortcuts. That plugin wasn't implemented by me, but there were some bugs and the code needed refactoring.</p>

![GSOC](/img/krita_ten_brushes_plugin.png)

<b>What was implemented?</b>

- Write and Read Settings methods
- Clean up tenbrushes.py
- Iterate using enumerate
- Initialize method to setup GUI components
- Idiomatic imports
- Keep actions alive
- Fix bug when adding new brushes after write settings
- loadActions method
- Accept method from dialog is calling writeSettings now


<b>Testing</b>

<p style="text-align: justify;">Below, you can see a gif to understand how the plugin works.</p>

![GSOC](/img/ten_brushes_plugin.gif)


### Last Documents Thumbnails Docker

<b>Concept</b>

<p style="text-align: justify;">The Last Documents Thumbnails Docker is a simple Docker that shows the recent documents thumbnails. Until the moment, the Docker is read-only, then you can just visualize the thumbnails, but I'm intending to implement new features in the future.</p>


<b>GUI implementation with PyQt</b>

<p style="text-align: justify;">You can see below the final result of my work. It's QWidget with a horizontal scrollbar where the QImages are rendered and we have a QPushButton to refresh the current list of recently opened documents.</p>

![GSOC](/img/last_documents_docker.png)

### Implement Ten Scripts Plugin

<b>Concept</b>

<p style="text-align: justify;">The Ten Scripts Plugin is pretty similar to Ten Brushes Plugin, but instead of brushes, you assign scripts to be executed. You point the action to a module python and that module will be executed when the shortcut is pressed. The triggered action will find a <b>main</b> function to be executed if there are that function declared. The assigned scripts keeping working even when the application is restarted using saved settings.</p>

<b>GUI implementation with PyQt</b>

<p style="text-align: justify;">You can see below the final result of my work. It's a QGridLayout with ten rows and three columns. QLabel (it shows the shortcut), QLineEdit (read-only to show assigned path of the script) and QPushButton (when pressed, it opens QFileDialog to select the python script).</p>

![GSOC](/img/ten_scripts_plugin.png)

<b>Testing</b>

<p style="text-align: justify;">Below, you can see a gif to understand how the plugin works.</p>

![GSOC](/img/ten_scripts_plugin.gif)


### Experience and next goals

<p style="text-align: justify;">It was an amazing experience and I'm really happy to have the opportunity to make part of the Krita community and help the users to have a better experience. I learned a lot along of this months, not just about code, but about goals, priorities, and people. KDE and Krita remind me every day, why I keep coding and why I'm doing what I'm doing.</p>

<p style="text-align: justify;">I'm intending to keep contributing to Krita with new plugins/scripts, extending Python API and writing documentation to a better experience to users and devs.</p>

<p style="text-align: justify;">Thank you</p>
