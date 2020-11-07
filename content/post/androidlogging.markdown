---
layout: post
title: Android Logging
date: 2015-12-25 00:32:41.000000000 +05:30
type: androidlogs
date: 2015-12-25T00:00:00-00:00
draft: false
---

Logging will be really helpful for debugging.
Below are the types of logs that can be used in Android Development.

* Verbose- Should never be compiled except during development
* Debug - They are compiled but are stripped
* Info, Warn and Error- Will be always available

Verbose mode provides and show all the logs level

###Syntax

* Verbose - `log.v(logtag,logmessage)`
* Debug - `log.d(logtag,logmessage)`
* Info - `log.i(logtag,logmessage)`
* Warn - `log.w(logtag,logmessage)`
* Error - `log.e(logtag,logmessage)`

