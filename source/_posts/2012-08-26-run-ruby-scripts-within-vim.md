---
layout: post
title: "Run Ruby Scripts within VIM!"
date: 2012-08-25 11:41
comments: true
categories: 
- ruby
- vim
---

Since I'm writing lots of Ruby scripts lately I was tired testing them using the Command Line and MacVim. 

Saving the file, go to to terminal, reuse last command `$ ruby foobar.rb`

> to slow and boring!!!

Fortunately I found out it is possible to run Ruby Scripts inside VIM with the following 2 commands:

``` vim
:set makeprg=ruby\ %
 
:make
```

If you are lazy like me put something like this in your .vimrc and run your scripts blazingly fast (3 keystrokes)!

``` vim
map <Leader>rr :set makeprg=ruby\ %<cr>:make<cr> 
```

If you use RVM and want to use a specific version of your installed rubies you can go with something like this:

``` vim
map <Leader>rr :set makeprg=~/.rvm/bin/ruby-1.9.3-p194\ %<cr>:make<cr>
```
Of course this works with other scripting languages as well e.g.:

``` vim
map <Leader>rp :set makeprg=python\ %<cr>:make<cr>
```
