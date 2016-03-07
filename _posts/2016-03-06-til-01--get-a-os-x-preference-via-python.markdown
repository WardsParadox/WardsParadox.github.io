---
layout: post
title: "TIL 01 - Get a OS X Preference via Python"
date: "2016-03-06"
tags: ["TIL","Python"]
---

As I am trying to learn more of the Python programming language (version 2.7.* as that is what is currently built-in to OS X), I find little challenges to help process what I have learned of it. Recently I was introduced to the `Foundation` frameworks that come with OS X. For a while I was writing scripts that required `plistlib` which could only read the XML version of a plist. OS X stores preferences in binary plist form. In order to use `plistlib` then, I was shelling out using `subprocess` and converting the plist to xml form temporarily. As I am trying to stay away from some of the "bad Mac Admin" practices, I found myself needing a way to read preferences without messing with the hard files. I could use `subprocess.check_output` and read the results of defaults, but why add more complexity (just my opinion). Here is what I came up with (this example uses the Munki preference file):

{% gist wardsparadox/a678cb2e1187923b97e7 getpreference.py %}
