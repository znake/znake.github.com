---
layout: post
title: "Issues with ZSH and Octopress"
date: 2013-03-08 21:02
comments: true
categories: 
- zsh
- octopress
---

Since I moved from bash to zsh I figured out some commands for Octopress stopped working. 

E.g. when I run rake deploy I get this:
``` bash
$ bundle exec rake deploy
zsh: correct 'deploy' to '_deploy' [nyae]?
```



To get rid of the annoying message I now use some commands with quotation marks like this:
``` bash
# deploying
$ bundle exec rake deploy
->
$ bundle exec "rake deploy"

# installing new themes
$ bundle exec rake install[slash]
->
$ bundle exec rake "install[slash]"

# generating a blog post
$ rake new_post[Issues with zsh and Octopress]
->
$ rake "new_post[Issues with zsh and Octopress]"
```
