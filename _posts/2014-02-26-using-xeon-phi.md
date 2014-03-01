---
layout: post
title: Using the Xeon Phi rack!
---

Back in October, 2013 the department acquired a special new computer from Intel containing four of their new [Xeon Phi coproccessors](http://ark.intel.com/products/75801/Intel-Xeon-Phi-Coprocessor-5120D-8GB-1_053-GHz-60-core). 

Now after months of sitting idle the Xeon Phi rack is setup and configure for us to work with!

##Lets get started!

To get running on the Xeon Phi you'll need a couple of things:

1. A user account
2. Git
3. [Cygwin](http://www.cygwin.com/) (for windows users)
4. [MSysGit \(Git Bash\)](http://msysgit.github.io/) (for windows users)
5. Copy your .ssh keys to the server
6. Our super handy `setup_project.sh` script

### 1. Getting a user account

To get a user account simply contact:

1. [Joss Whittle](mailto:637342@swansea.ac.uk?Subject=Xeon%20Phi%20access) (Me) - I sit at the desk next to the 4th floor kitchen / the printer
2. [Damion Theobald](mailto:637342@swansea.ac.uk?Subject=Xeon%20Phi%20access) - You can find him in the IT Room on 4th floor

### 2. Install Git

This can be any version you like, on Windows I highly recommend the [Github for Windows](http://windows.github.com/) app. That being said, said for setting up a new project on Windows you'll still need the Cygwin & MSysGit tools so you can run Bash Scripts.

### 3 & 4. Install Cygwin & MSysGit

**Cygwin** is a Bash Shell for Windows which allows you to run many of the native linux command line programs such as SSH, Git, ssh-keygen, and many more. 

We've built a `setup_project.sh` script which does all the hard work building your local project repo and linking it to a remote repo on the Xeon Phi host. But to run this script you need to be able to execute Basg scripts. *(If someone would like to port this script to run under Windows Powershell, please see the repo linked below!)*

**MSysGit** is a Bash Shell client for Git which has been specifically tailored to work flawlessly under Windows & Cygwin.

### 5. Copy your .ssh keys over to the Xeon Phi host

<p class="message">
	**Note:** This only needs to be done once per computer you wish to develop on.
</p>


There's nothing more annoying than re-typing your password every time you try to push code to the Phi Host. To combat this, setup passwordless ssh by copying your local public key into the Xeon Phi's `authorized_keys` file. 

<p class="message">
	**Note:** On windows under Cygwin, you local .ssh folder with your public key will be stored in "C:/users/[username]/.ssh/>"
</p>

On windows, or if you haven't previously generated ssh keys before on your *nix system; open a terminal (Cygwin on Windows) and run:

	$ ssh-keygen -t rsa

You'll then be prompted to enter a pass-phrase **DO NOT TYPE ANYTHING**, simply press enter, then enter again to confirm your blank password. 

Next, ssh into the Xeon Phi Host append your **public key** file to the `authorized_keys` file in your home directory ( `~/.ssh/` ).

	$ cd ~/.ssh/
	$ echo "paste-your-public-key-here" >> authorized_keys

<p class="message">
	**Note:** The double right arrow above is important! This means "append" rather than "replace" so you won't lose any previous keys added.
</p>