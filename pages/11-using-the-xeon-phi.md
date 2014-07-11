---
layout: page
title: Using the Xeon Phi rack!
categories: [xeon_phi]
---

Back in October, 2013 the department acquired a special new computer from Intel containing four of their new [Xeon Phi coproccessors](http://ark.intel.com/products/75801/Intel-Xeon-Phi-Coprocessor-5120D-8GB-1_053-GHz-60-core). 

This post goes over setting up your local development environment for working with the Xeon Phi and basic rules and workflow for running your programs.

------

##Lets get started!

To get running on the Xeon Phi you'll need to install & do a couple of things:

1. Get a user account
2. Git
3. [PuTTY](http://www.putty.org/) (for windows users)
4. [UltraVNC Viewer](http://www.uvnc.com/) 

------

### 1. Getting a user account

To get a user account simply contact [Joss Whittle](mailto:637342@swansea.ac.uk?Subject=Xeon%20Phi%20access) (Me) - I sit at the desk next to the 4th floor kitchen / printer. Please send emails from your university account for transparency. Once we've got permission to add you to the system, I'll email you your login details and the ip address.

### 2. Install Git

Writing code to run on the Xeon Host or Coprocessors is difficult, so much so that it will take quite a bit of practice and trial and error. Save yourself the headache and version your projects with Git. This also has the benefit of letting you work locally on your own system, and then push to compile your code on the Xeon host. 

### 3. Install PuTTY

**PuTTY** is an SSH/Telnet client for Windows. It allows you to connect to the command line of the Xeon host or coprocessors without needing a bulky gui interface. Please take care to use SSH over VNC when running commands which can end your VNC session abruptly, such as `$ service vncserver restart`. Running this command while logged in over VNC will close your connection immediately and stop the vnc server from restarting correctly. 

### 4. Install UltraVNC

**UltraVNC** is a remote desktop software which works really well for connecting to Xeon Host over the departments local network. 

------

###Rules

What would be something fun without rules! Right guys? Right... 

Anyway, this system is an expensive piece of kit, and we have to take care of it and use it properly. The key thing to remember is:

<p class="message">
	If you have to question whether you'll be in trouble for doing `X`, don't do that.. :p
</p>

Everything else is mainly housekeeping and common sense, such as letting people know if you're running a big job.

If you're going to run a job on the Phi Host or one of the cards for a long period of time, please send a quick email to the research group, or at least [Joss Whittle](mailto:637342@swansea.ac.uk?Subject=Xeon%20Phi%20access) (me), to let people know not to do any maintainance or run our own jobs too.

## That's it, happy coding and give us a shout if you have any questions! :)
