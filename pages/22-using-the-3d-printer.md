---
layout: page
title: Using the 3D Printer!
categories: [3d_printing]
---


We have a [MakerBot Replicator 2X](http://store.makerbot.com/replicator2x) 3D printer available in the department for research purposes, currently in the server room on the 3rd floor of the Faraday Tower. What does the *X* mean? Basically that it is "experimental", in that it has:

* dual extrusion, i.e. being able to print in two colours or two materials at once, and 
* a heated bed that enables you to print with plastics like ABS.

------

##How do I get started?

First, you need a 3D model to print. There are various CAD packages available to make 3D models. As a programmer you'll probably like [OpenSCAD](http://www.openscad.org/), which allows you to create a parametric script that compiles into a 3D model. 

Have a look at [this article](https://medium.com/p/3d28fd9b068c) that shows you how to get started with OpenSCAD and MakerWare by designing an enclosure for a Raspberry Pi. The design files for the enclosure can be [downloaded from Thingiverse](http://www.thingiverse.com/thing:201867). 

There are a lot of great designs on Thingiverse, so have a look there for some OpenSCAD script examples and models. You'll probably find that someone has already designed something similar to what you have in mind, so use their design as a base to work from and be sure to give them credit!

------

##I have a 3D model, what now?
Export your 3D model as an .STL file and load it up in [MakerWare](https://www.makerbot.com/makerware/). When you open MakerWare, click the "Add" button to load your .STL file. You can see where on the build plate your object will be built, and you can move, scale and turn the object using the controls on the left. When you’re ready to send it off to the printer, click "Make", make sure the right material (PLA/ABS) is selected and adjust the settings as necessary. We have both ABS and PLA filament available. 

<p class="message">
Note: Printing in ABS is preferred at the moment (3/14), as the filament extruder on our printer sometimes get stuck when using PLA.
</p>

Under the "Advanced Options", there is a checkbox for "Use Preview before printing". This is very useful if you’d like an estimate of how much material will be used to print your object, as well as an estimated time to print.

Click "Export" and save the resulting .X3G file (on an SD card if you have one).

------

##OK, I have a .X3G file.
Before you use the 3D printer for the first time, please send an e-mail to [Gerrit Niezen](mailto:g.niezen@swansea.ac.uk?Subject=Departmental%203D%20printer) (me). I'll help you set up your print and try to help sort out any issues. Also please send me an e-mail if you'd just like to chat about your idea or if you have any questions. 

If you like to play around with 3D printers in your free time, go and check out [Swansea Hackspace](http://swansea.hackspace.org.uk).
