---
layout: post
title: GSoC - Community Bonding Period with Krita
color: blue
subtitle: Part two
tags: ['KDE','GSoC','Krita']
date: 2017-05-29 00:30:00
---

Hi everyone, is everything ok? I hope so.

<p style="text-align: justify;">Today, I will talk about my week working on Krita during this community bonding period that ends this Wednesday.</p>

<p style="text-align: justify;"> I will try to be more concise this week and I will explain what I've made in a short list.</p>

### 1. Unit tests to Python scripting API

I made previously, the [integration](https://phabricator.kde.org/D5675) of python tests with [cmake](https://cmake.org/Wiki/CMake/Testing_With_CTest). Now, I implemented tests to all classes that don't need a GUI to work, at least partially. I wrote tests to classes below:

* Action
* Filter
* InfoObject
* Extension

When you implement tests, you naturally find errors. I found some inconsistencies that I fix, but I need to understand others behaviors, like setConfiguration method in the Filter class.

Reviews([D5967](https://phabricator.kde.org/D5967) and [D5982](https://phabricator.kde.org/D5982)) created and commits pushed to my remote branch.

### 2. Improve Scripter plugin

<p style="text-align: justify;">As I told in my <a href="https://eliakincosta.github.io/2017-05-14-introduction-gsoc-2017-with-krita/">introduction</a> for GSOC, I'm intending to use the Scripter to execute and edit scripts.</p>
<p style="text-align: justify;">When I started to work in this plugin, we was using the exec function(python 3) in python to run all the code from the editor, but it's really more complex to implement and maintain the scripter using exec, mainly when using files where we can create classes and all.</p>

<p style="text-align: justify;">Now the implementation creates a python module to refer to files, but the Scripter still using exec when the code is executed without saving files. You can see a peace of code below:</p>

```python
if document:
    spec = importlib.util.spec_from_file_location("users_script", document.filePath)
    users_module = importlib.util.module_from_spec(spec)
    spec.loader.exec_module(users_module)
    users_module.main()
else:
    code = compile(script, '<string>', 'exec')
    empty_scope = {}
    exec(script, {})
```

<p style="text-align: justify;">If you need more details about my reasons to take this decision please read this <a href="https://phabricator.kde.org/T5885#95717">comment</a> in the task thread.</p>

### 3. Krita community 

* I'm following other tasks in the Krita to know what people have made.

* Talking with my mentors to understand some important implementations.

* Reading [documentation](https://api.kde.org/bundled-apps-api/calligra-apidocs/krita/libs/libkis/html/inherits.html) to libkiss. Thanks, Wolthera :).


That's it for now, until the next week. See ya!!
