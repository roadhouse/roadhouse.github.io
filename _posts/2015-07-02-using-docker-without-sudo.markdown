---
layout: post
title: "Using Docker Without Sudo"
date: 2015-07-02T15:47:32-03:00
---

i have this error:
```
FATA[0000] Get http:///var/run/docker.sock/v1.17/info: dial unix /var/run/docker.sock: permission denied. Are you trying to connect to a TLS-enabled daemon without TLS?
```

it's occur because my user is not in docker group, to fix:
```
sudo usermod -a -G docker $USERNAME
newgrp Docker
 ```

the last command login in the docker group in the current shell

