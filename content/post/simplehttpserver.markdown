---
layout: post
title: Simple HTTPServer in Local Machine
date: 2013-08-25 18:38:16.000000000 +05:30
type: devlogs
date: 2013-08-25T00:00:00-00:00
draft: false
---
I was trying to setup a local [webserver](http://en.wikipedia.org/wiki/Web_server).
I need it because, I was learning [D3](http://en.wikipedia.org/wiki/Protovis#Context) a javascript library after getting to know about it from Geeks Night session.

First I was downloading MAMP, but due to awesome internet connectivity I almost lost my patience since it was taking more than 40 minutes to download. On searching in internet for other options I found that there is a charm in Mac OS X due to preinstalled Python.

If we are trying with HTML,CSS and javascript this option will be very usefull.
Try the below in Terminal Window
`python -m SimpleHTTPServer <port-number> &`

This will start a local HTTP server in your Mac.
Access it via browser in below url
`http://localhost:<port-number>/`

In order to shutdown the server just close the Terminal window.

I learned it from this [link](http://www.linuxjournal.com/content/tech-tip-really-simple-http-server-python)

I am very late in learning this :(

