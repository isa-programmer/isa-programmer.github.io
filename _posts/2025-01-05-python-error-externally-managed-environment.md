---
layout: post
title: How to solve pip error externally-managed-environment in linux?
subtitle: pip externally-managed-environment
thumbnail-img: https://www.python.org/static/img/python-logo.png
tags: [python,linux,error,pip,programming]
author: Isa
---
Hello programmers! You may get this error in pip:
~~~
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.

    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.

    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.

    See /usr/share/doc/python3.11/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
~~~

###So how can we solve this error?

We have 2 option for this

#### Using pipx
~~~
sudo apt install pipx #install pipx
pipx install numpy #install the library with pipx
~~~


#### Enabling break system packages option for pip
Use this command to enabling break system packages for pip
~~~
python3 -m pip config set global.break-system-packages true
~~~


if you want undo this setting
~~~
nano ~/.config/pip/pip.conf #nano or any code editor


[global]
break-system-packages = true #change to 'false' if you want disable break system packages
~~~
