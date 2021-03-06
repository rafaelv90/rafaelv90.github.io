---
layout: post
title:  "Creating a bootable Mac OS X flash drive"
date:   2015-09-30 23:00:00
categories: mac
author: Rafa Valério
---

Upgraded your MacBook with a new SSD? Want to update the OS to El Capitan with a clean install?

![Mac OS X El Capitan](/assets/posts/el-capitan.jpg)

The best (and fastest) way to do this, is using a bootable USB flash drive with the desired version of Mac OS in it.
You will need the installer of the desired version of Mac OS and a USB flash drive with at least 8GB of space (The drive will be completly erased before the process).

**Starting**

You can download the installer of the Mac OS version you want, using the App Store.

Then you need to use a tool called createinstallmedia, that can be found inside the installer of Mac OS X, to create a bootable pendrive.

Open your favorite terminal app, and type:

{% highlight bash %}
sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app
{% endhighlight %}

**What happened?**

We called the createinstallmedia tool, sending two parameters:

1. volume: This is a path to the volume (USB flash drive) that will be used

2. applicationpath: This path leads to the installer app itself, in my case “Install OS X Yosemite.app”

**Installing Mac OS X from flash drive**

All you need to do is reboot your Mac OS X, with the USB flash drive plugged in, and keep the option key pressed down.

Then you’ll be able to choose your new flash drive as a boot option, and follow the instructions on screen.
