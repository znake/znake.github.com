---
layout: post
title: "Issues with zsh and Octopress"
date: 2013-03-08 21:02
comments: true
categories: 
- zsh
- octopress
---

Since I moved from bash to zsh I figured out some commands for Octopress stopped working. 

E.g. when I run `$ bundle exec rake deploy` I get `zsh: correct 'deploy' to '_deploy' [nyae]?`

To get rid of the annoying message I now use some commands with quotation marks like this:
`$ bundle exec "rake deploy"` or `$ bundle exec rake "install[slash]"` to install a new theme or for a new blog post `$ rake "new_post[Issues with zsh and Octopress]"`. 
