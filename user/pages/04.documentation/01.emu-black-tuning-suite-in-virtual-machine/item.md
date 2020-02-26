---
title: 'EMU Black Tuning Suite in Virtual Machine'
media_order: 'virtualbox-gui.png,add-extensions.png,tuning-gui.png'
taxonomy:
    tag:
        - 'EMU Black'
---

# Preface
This is a step by step guide to get the EMU Black tuning software working inside a virtual machine on any operating system. Largest use case for this is anytime you need to install the EMU Black tuning sofware on a non Windows machine. This entire setup is free to download and use.

!!! You will need around 8GB of free space on the machine you are setting this up on. If you don't have that much space trying deleting some unneeded files or emptying the trash/recyling bin.

# Download and install required tools
* VirtualBox - [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
  * visit this page and download the latest version for whatever operating system you are installing on. For myself I use a Mac computer.
* Vagrant - [https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html)
  * same as above. For most users you will want the "64-bit" version.
* VirtualBox Extension Pack - [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
  * look for the "All supported platforms" link and download the file once clicked for later use. Be sure that you are downloading the same version as step 1 above.

# Setting up the VM supporting packages
Once you have installed all of the items above you should be able to access the VirtualBox interface by starting up the program. On my mac I simply press the command and spacebar together, search VirtualBox and hit enter. You should see something like below sans anything in the left column.
![Virtual Box GUI](virtualbox-gui.png?lightbox)

Once you are here you need to click through the menus and to go VirtualBox->Preferences->Extensions. Should look like below.
![Add extensions dialog](add-extensions.png?lightbox)

Click the little green plus icon on right right side and select the file that you downloaded previously. Should be something like "Oracle VM VirtualBox Extension Pack". Once that succeeds you can close out of all of those windows.

# Configuring local files and folders
All that's left is to run a few commands to get everything up and running. I will attempt to cover how to do this on major operating systems.
## Step 1
First we need to open up a command line program. Below is how to do it for each major operating system.
### Mac OSX and Linux
```
Open a Terminal program window (not a command)
```
### Windows OS
```
Open a Command Line prompt (not a command)
```
## Step 2
Point your system to your Documents folder so we can build some files. Copy, paste and hit enter in your command line window opened in previous step.
### Mac OSX and Linux
```
cd ~/Documents
```
### Windows OS
```
cd ~/[your-username]/Documents
```
## Step 3
Create a working directory for us to generate some files and for the virtual machine to live.
### Mac OSX, Linux and Windows OS
```
mkdir emu
```

## Step 4
All that's left to do is initalize and run the provisioning script. Copy and paste the commands below and run them individually.
### Mac OSX, Linux and Windows OS
```
cd emu
```
```
vagrant init ameeuwsen/emu-black --box-version 1.0.0
```
```
vagrant up
```
! This last command could take up to 10 minutes depending on how many resources your host machine has. Be patient and watch the magic.

## Ready to tune
![The EMU Black Tuning Suite](tuning-gui.png?lightbox)
Once all the above steps have been completed successfully you will have a full Windows 7 virtual machine with the EMU Black Tuning software preinstalled. Enjoy!
