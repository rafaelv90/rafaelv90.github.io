---
layout: post
title:  "Fixing the 'There is no connected camera' error on MacBooks"
date:   2014-11-19 13:30:00
categories: fix mac
---
Have you ever got the error "There is no connected camera" on MacBook?

![There is no connected camera.]({{ site.baseurl }}/assets/article_images/2014-11-19-fix-mac-os-camera-bug/mac-error.jpg)

I had this error a lot of times, and always restarted my Mac to fix, but then I decided to look for a better fix, then I find this.

When you launch apps that uses the webcam, a process called VDCAssistant is started to manage the camera use. This process can stop to work if you use the Mac with external monitors or in "clamshell" mode (with the lid closed) oftenly.

To fix, type this in your prefered terminal app:
{% highlight bash %}
  sudo killall VDCAssistant
{% endhighlight %}


Then just restart your app and the camera should work!

This command shut down the VDCAssistant, so it can be started again without errors.

Was this useful? Have questions? Call me at Twitter: [@rafaelvalerio][twitter].

[twitter]:       http://twitter.com/rafaelvalerio