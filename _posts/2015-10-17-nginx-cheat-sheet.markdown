---
layout: post
title: "Nginx Cheat Sheet"
date: "2015-10-17"
---

### nginx config paths

```shell
# server config
$ /etc/nginx/sites-available/<server-file>

# create a soft link to sites-enabled to activate your server
$ ln -s /etc/nginx/sites-available/<server-file-name> /etc/nginx/sites-enabled/<server-file-name>

# default www location
$ usr/share/nginx/html/
```

### nginx service

```
# restart nginx ubuntu
$ sudo service nginx status
$ sudo service nginx start
$ sudo service nginx stop
$ sudo service nginx restart
```

### Simple nginx directive to serve robots files

```
location /robots.txt {
    return 200 "User-agent: *\nDisallow: /";
}
```
