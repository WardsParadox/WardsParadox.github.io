---
layout: post
title: "TIL 02 - Multiple Inputs For One Argument"
date: "2016-06-05 15:43:30 -0600"
tags: ["TIL","Python"]
---

I use a tool called <a href="https://github.com/nmcspadden/OutsetDockProfiler/" target="_blank" title="This script creates a package to use with Outset that will install a user-level profile for a specific user of your choice.">Outset Dock Profiler</a> made by <a href="https://osxdominion.wordpress.com/" target="_blank">Nick McSpadden</a>. It's great and for user accounts where I only need to target one profile, it works great! {% icon fa-thumbs-o-up fg-lg %}


There has always been one thing about it that bothered me. If I had multiple profiles for a user, I couldn't use this tool. Sure I could use it to build an initial package and modify the script. I've done it before but it can be easy for me (my brain is the size of a pea after all) to forget. I decided to learn about{% ihighlight python %}argparse{% endihighlight %} and add the ability to use multiple profiles. Now not only does it support multiple profiles but it will also organize the profiles into the appropriate folders by username. This means that regardless of the number of profiles you need, as separating out the payload makes management of them easier, it will "install" them all as long as you have targeted the right user. Check it out on my github.
I am thinking about pull-requesting it back to Nick, but I'm sure there are other issues that I created. Let me know what you think.


<a href="https://github.com/wardsparadox/OutsetDockProfiler" target="_blank" title="My fork">My fork of OutsetDockProfiler</a>
