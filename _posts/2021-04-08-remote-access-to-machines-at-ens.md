---
layout: post
title: Remote Access to Machines at ENS
bdate: April 8, 2021 12:00 AM
author: Harsha S. Bhat
math: false
tags:
  - remotework
hide: false
---
- Make sure your machine is connected with Ethernet, you have your WiFi turned on and the machine is plugged to the power adapter.

- Contact Pierpaolo to get a fixed IP. He will explain how to set it up. 
- While you have him also ask him for an account in aragonite.ens.fr
- Get back to your machine and enable remote login. On a Mac
  - System Preferences --> Sharing --> Remote Login
- (macOS) Go to Sytem Preferences --> Energy Saver (or Battery in new version of MacOs) --> Enable 'Wake for network access'

Now you should be able to connect. To test and ensure this works properly you need to be outside the network. I simply use my phone's hotspot to get this done. 

The best workflow is to have all your codes and scripts executable from the terminal. Ideally they will spit out some images. Simply move those images to your Dropbox/Google Drive etc. folder. This way you dont have to sftp files back and forth as it is quite slow via aragonite.

## Don't want to leave your machine fully on all the time! 

Steps to connect.

1. ```ssh <username>@aragonite.ens.fr```
2. Enter your password
3. ```ssh <your-laptop-username>@<IP Address>```
4. Enter your password and you are connected.
5. Now launch your scripts.

One thing to keep in mind is that Dropbox doesn't seem to sync when the machine is sleeping. So after all your images are ready, in the terminal,

- type ```caffeinate -u -t 2``` to wake up the Mac
- Ensure that all the files are synced
- type ```pmset sleepnow``` to put the Mac back to sleep

### Always use stackexhange for your questions! It has never disappointed me so far!

