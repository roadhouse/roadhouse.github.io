---
layout: post
title: "Fix Problem on Zsh When Passing Params to Rake"
date: 2015-07-22T18:51:07-03:00
---

I have this error when execute a rake taks with params on Zsh:

`zsh: no matches found: my_namespace:my_task[my_param]`

So i add `unsetopt nomatch` to `~/.zshrc` to solve

[reference](https://robots.thoughtbot.com/how-to-use-arguments-in-a-rake-task)

