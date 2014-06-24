Hovercraft
==========

This is a prototype hovercraft for Unreal Engine 4 built in Blueprints.

Gameplay Video
==============

[![Video](http://img.youtube.com/vi/avZGdjGAkYg/0.jpg)](http://www.youtube.com/watch?v=avZGdjGAkYg)

Music by [Michael Hughes](http://michaelhughesmakesmusic.com)

Playable Demo
=============

Download and play the demo level:

* Mac: [download playable demo for Mac](https://s3.amazonaws.com/piinecone/github/hovercraft/Hovercraft-Mac.zip)
* PC: [download playable demo for Windows (64 bit)](https://s3.amazonaws.com/piinecone/github/hovercraft/Hovercraft-Win64.zip)

Details
=======

This repository doesn't actually contain the necessary **.uasset** and **.umap** files to load the project. You will need to download
an archive of the latest release below.

I'm currently using [blimp](https://github.com/piinecone/blimp), a utility I wrote for syncing large files to S3 alongside a git repo. It is neither
a true git plugin nor does it integrate with UE4, meaning you can't currently diff **uasset** files using the editor. I will look into setting up an open
source Perforce repository, though I would like to figure out a way to manage the project with github.

Project Source & Installation
=============================

I haven't determined the best way to open source a codebase with large binaries, so for now I'm just archiving and tagging releases:

* Archive of the latest codebase: [hovercraft-a9d2788.zip](https://s3.amazonaws.com/piinecone/github/hovercraft/Hovercraft-a9d2788.zip)

Usage & Configuration
=====================

Once you've loaded the project, you should be able to select the **Hovercraft** blueprint and migrate it to another project from the context menu.

Caveats & Issues
================

There are several issues at this stage, collisions being the most apparent. Other problems include but are not limited to:

* Sputtering while idling (antigrav)
* Friction values
* Physics object impact forces

Collision Bugs
--------------

I plan to take a second pass on collisions for the next release.

* The math for the collisions feels like it is definitely wrong, being overly complex and unintelligible
* The collider is misshapen and it's possible that the components hierarchy is flawed
* There is a rotation effect that occurs during a collision that can cause looping revolutions

Todos
=====

* Better version control
* Fix Collisions
* Add jump/vertical thrust limits
* Add sound effects
* Parameterize and document all variables
* Better blueprint export/import workflow
* Animate the hull during impact
* Add surface particle effects
* Simulated physics implementation using forces instead of translation

Contributing
============

* Fork the repo
* Download the project source
* Make some changes on a feature branch
* Issue a pull request and we'll figure it out from there

License
=======

Released under the [MIT License](http://opensource.org/licenses/MIT)
