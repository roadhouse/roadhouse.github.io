---
layout: post
title: "Fix problema with screen"
date: 2017-03-09T15:27:32-03:00
---

in my daily work logging in servers i caught this error:

```
Cannot open your terminal '/dev/pts/0' - please check
```

it's occur because the current shell was already initialized (probably because use of `sudo su`), and the screen going crazy, to fix do this:

`script /dev/null`

yeah, it's a unix-command-line-hack, but works, if you are curious about why this works, see this [thread](http://serverfault.com/questions/116775/sudo-as-different-user-and-running-screen/116830#116830)
