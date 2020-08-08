Default design theme for Net-at-hand
====================================


Included files
------------------------------------
This is the default design theme for Net-at-hand sites. The included files
are:

* README.md - this file
* build/stucture/head.html - content that needs to be placed in the HTML head area
  for the design theme
* build/structure/structure.html - content for the page structure section of the design
  theme
* build/styles.css - css file for the 
* build/stylesheets/design_images/340/asphalt.jpg - image used for html within the CSS file



How to use this repository
--------------------------
**Step 1--Set your computer up.**
This repository assumes you have a node environment set up with yarn as a package manager
and git installed for source control.
If you know what that means, then you can just clone this repo and get to work.  If
those words mean nothing to you, we've [got a page set up](http://dev.nah.onl/setting-up-a-development-environment) 
explaining the step-by-step process of setting all this up.

**Step 2--Clone the repository**
In a terminal window cd your home directory (or whatever directory you want to work in)

    cd ~

Then clone this repository to download it:

    git clone git://github.com/nah-dev/nah-default

**Step 3--install the node packages**
Once it is cloned, then cd into the nah-default folder and install the necessary
node packages to run the environment:

    cd ./nah-default
    yarn install

If all goes well, you'll see a bunch of text fly down the terminal window,
and you wont see anything near the end of it that says something like "failed"
or "error".

**Step 4--start up the "system"**
While still in the nah-default directory do this

    yarn run watch

You'll see some more text come up as the gulp system starts up and then your
default browser should open up a new window pointed to "http://localhost:8080".

**Step 5--modify files and see what it looks like**
From here you can navigate to the sample files.  Any changes you make to the files
within the source folder will be processed and converted to .css and .html files
within the build folder.

The top of ./build/styles.scss has some sass variables that you can modify and
you'll see the changes within the sample files very quickly.

One of the first variables in style.scss is the directory location for your
design theme's image file.  You'll want to change this to whatever the
directory is within your Net-at-hand design theme.  For the sample pages, the
images should be in the ./build/images folder. The .scss variable $image-location
is set to this folder for the sample pages. It get's overriden by whatever you
set it to is ./source/styles.scss for the main stylesheet that you copy and 
paste into your Net-at-hand design theme.

**Step 6--mess up and revert**
The great thing about having this in a version control system is that you can revert
changes that you've made.  So, for example, you can modify ./source/styles.scss
and tear it apart.  Mess it up.  Then in the terminal, cd into the project
directory and type

    git checkout ./source/styles.scss

This will revert it back to what the file was when you first checked it out.
This document isn't meant to teach you how to use git, but if the idea of
commiting small changes to a file and safely having all versions of that 
file available for reference and to revert to you should find a git tutorial
and learn how to use it.

One last note on this, if the whole thing is a mess and you just want it all
to go back to the way it was when you first cloned it (assuming you haven't
committed any changes), just type

    git reset --hard


Sample header images
------------------------------------
A sample header image and the styles for using it in the header are included
for your reference.  To use it, just uncomment the line in ./source/styles.scss
that imports the _header-images.scss file:

    @import "styles/_header-images.scss

With this file included, the header is modified to include three header images
at three different screen sizes. By default it is anchored to the bottom left of
the header, but you can change this and also change the scaling behavior to
achieve whatever layout you want with the image.



Change log
------------------------------------
Changes made to this design theme

* 1.7 - Added sample header images
* 1.6 - Set up better sample pages
* 1.5.2 - bug fix
* 1.5.1 - bug fixes
* 1.5 - set up project to use gulp 
* 1.0 - initial release


License
------------------------------------
This work is distributed under a Creative Commons Attribution-ShareAlike 
3.0 license.  You are free to use the work in any way that you wish.
[http://creativecommons.org/licenses/by-sa/3.0/deed.en_US]

Note that the asphalt.jpg image was derived from Subtle Patterns 
[http://subtlepatterns.com/asfalt/]