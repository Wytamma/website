---
title: "Using VScode to access the HPC"
date: 2020-08-03T00:00:00-00:00
excerpt_separator: "<!--more-->"
header:
  image: assets/images/vscode-hpc.png
categories:
  - blog
tags:
  - workflow
  - hpc
---

One of the biggest hurdles to using a the high performance computer (HPC) at JCU is the user interface. Researchers have to ssh into the HPC via the command line. This, command line only, interface can be very different from the day to day computer experience researchers are used to. To ease the transition to remote computing on the HPC I suggest that researchers should use an integrated development environment (IDE) to access the HPC.

An IDE is basically a file explore, a text editor, and terminal all in one. There are many types if IDEs, many the one most researchers would be used to is RStudio. While RStudio is an excellent IDE for R programming it is very specific. A more general IDE is visual studio code (VScode).

> Worldwide, Visual Studio is the most popular IDE, Visual Studio Code grew the most in the last 5 years... <cite><a href="https://pypl.github.io/IDE.html"> Top IDE index</a></cite>

[VScode](https://code.visualstudio.com/) is a fully featured IDE produced by Microsoft. VScode is open source and quickly become the default for IDEs. Check out the [Github repo](https://github.com/microsoft/vscode).

## Use VScode to access the HPC

[Download VScode](https://code.visualstudio.com/Download) and start to get a feel for how it works on you local machine. There's some very good [docs](https://code.visualstudio.com/docs/getstarted/introvideos) on how to get started. 

![ssh-readme](../assets/images/ssh-readme.gif)

Because it is open source VScode is easily extendable. VScode has a an [extensive library of extensions](https://code.visualstudio.com/docs/editor/extension-gallery). One extension of note is [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) developed by Microsoft. This extension lets you connect VScode to a remote server (like the HPC) via SSH.

![extensions-view-icon](../assets/images/extensions-view-icon.png) Use the extensions tab to install Remote - SSH. Once it's installed a new tab (Remote Explore) appears on the side panel. Press the plus (+) in the Remote Explore tab to add a new SSH target for the HPC.

![ssh-command](../assets/images/ssh-target.png)
Only include -p 8822 if you are of campus. 

You'll be prompted for your HPC password; enter it and connect to the HPC. In the Explore tab you can now open folders and files on the HPC. Copying files to the HPC or back to you local machine is as easy as dragging and dropping them into the Explorer panel. If you open a new terminal (control+shift+`) you'll be dropped into a terminal on the HPC. 

When you're finished you can simply save and close VScode. Any changes will be on the HPC. To reconnect, open VScode and go to the Remote Explore panel click on `zodiac.hpc.jcu.edu.au` to reconnect to the HPC. 

For more information check out the Remote - SSH docs or [this helpful blog](https://code.visualstudio.com/blogs/2019/07/25/remote-ssh). 