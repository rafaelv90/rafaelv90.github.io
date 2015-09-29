---
layout: post
title:  "Fixing the 'There is no connected camera' error on MacBooks"
date:   2015-09-28 22:00:00
categories: mac
author: Rafa Valério
---

Have you ever got the “There is no connected camera” error on MacBook?

![There is no connected camera](/assets/posts/camera-error.jpg)

I had this error a lot of times, and always restarted my Mac to fix, but then I decided to look for a better fix and found this:

When you launch apps that uses the webcam, a process called VDCAssistant is started to manage the camera use. This process can stop to work if you use the Mac with external monitors or in “clamshell” mode (with the lid closed) oftenly.
To fix, type this in your prefered terminal app:

{% highlight bash %}
  sudo killall VDCAssistant
{% endhighlight %}

Then just restart your app and the camera should work!

This command shut down the VDCAssistant, so it can be started again without errors.
