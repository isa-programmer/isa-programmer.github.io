---
layout: post
title: A simple socket library for C
subtitle: CZMQ library
thumbnail-img: https://zeromq.org/images/logo.gif
tags: [c,socket,zeromq]
author: Isa
---
## Hello programmers!
As we know, socket programming in C can be very difficult, especially if you are a beginner.
For socket programming we use socket.h or winsock2.h libraries, but these are platform specific and can be difficult.
But don't worry, I will show you the czmq library, which is an easy and cross-platform library.
## Let's start!
### Installing library on your system
Download the czmq library according to your operating system
#### Debian/Ubuntu
~~~
apt install libczmq-dev
~~~

#### Fedora
~~~
dnf install czmq-devel
~~~

#### MacOS
~~~
brew install czmq
~~~

#### Windows (Using vcpkg)
~~~
.\vcpkg.exe install czmq
~~~