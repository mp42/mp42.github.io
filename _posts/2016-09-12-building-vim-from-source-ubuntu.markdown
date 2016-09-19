---
layout: post
title:  "Building Vim 8 From Source on Ubuntu 16.04"
date:   2016-09-12 22:16:57 -0700
categories: general vim
---

[Vim 8](https://groups.google.com/forum/#!topic/vim_announce/EKTuhjF3ET0) was recently released and I thought what better timing then to review how to build
Vim from the source! (_Note: this serves mostly as a note to myself on how to do this_). 

For the most part, I found [Valloric's excellent guide](https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source) to be complete even though it is specifically for an older version of Vim. Here are the steps I went through (with information from Valloric's guide):

1. Deleting the current version of Vim (_step #2 on Valloric's guide_)
2. Double checking that all prerequisite libraries (_step #1 on Valloric's guide_) are installed
	* this is an important step if we wish to build Vim with some language-specific support e.g Python 3, Lua etc.
	  

3. Checking out with source code and installing it
	* I usually use `sudo checkinstall` out of habit (using `checkinstall` generates a `.deb` which allows your package manager to uninstall vim for you).
	* I had issues building Vim 8 from source with support for both Python2.5 and Python3. After a bit of twiddling, I discovered that I could only build Vim 8 with support for **either** one only.
4. Setting the newly installed Vim as the default text editor
5. Removing the downloaded source directory
	* Completely optional but I like to minimize the amount of cruft I keep anyways. Do note that if you used `sudo checkinstall` the `.deb` package will be in the source directory. Move it somewhere else if you would like to keep it.
