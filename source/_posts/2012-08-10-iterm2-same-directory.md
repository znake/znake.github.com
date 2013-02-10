---
layout: post
title: "iTerm2: Stay in the same directory"
date: 2012-08-10 11:41
comments: true
categories: 
- iTerm
---

{% img center https://github.com/znake/znake.github.com/blob/master/images/iterm2/logo.png?raw=true logo %}

I use iTerm2 for about a year now but recognized one "hidden" handy feature just some days ago. 

If you cd in a directory where you might want to run a server, run your tests, use your VCS of choice and so on you need to open the same directory over and over again in your tabs or split panes. Open a new Tab and cd to the same directory all the time is very wasteful. So I´ve written a script which does that for me and bundled it with Spark so I just needed to type a shortcut to open a new Tab and cd to my current directory. 

BUT with iTerm2 you can achive this behaviour very easily: 

Go to Preferences -> Profiles -> General -> Working Directory -> Advanced Configuration -> Edit

![first](https://github.com/znake/znake.github.com/blob/master/images/iterm2/-1.png?raw=true)

Then you´ll be in this menu:

![second](https://github.com/znake/znake.github.com/blob/master/images/iterm2/-2.png?raw=true)


And change the Radio Button to Reuse previous session´s directory and you´ll get the automatic cd of your current directory for free!

 

UPDATE:

If you use zsh & RVM you want to add this line to your .zshrc:

 

__rvm_project_rvmrc

[https://rvm.io/integration/zsh/](https://rvm.io/integration/zsh/)
