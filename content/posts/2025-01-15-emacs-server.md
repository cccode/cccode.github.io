+++
title = "Emacs Server"
author = ["Christina Conway"]
date = 2025-01-15T23:19:00+00:00
lastmod = 2025-02-20T22:27:25+00:00
tags = ["performance", "emacs"]
draft = false
license = ""
+++

Emacs can be run as a server and client rather than just a single process. The biggest advantage of running emacs
in this way is that the client starts instantaneously, a huge performance boost.

The emacs server can be started with the following command:

> **emacs --daemon**

There are a few options that can be used to start the emacs server.
With **--fg-daemon["&lt;server name&gt;"]**, Emacs stays bound to the terminal,
so you can terminate it by pressing **Ctrl-C**. With **--bg-daemon["&lt;server name&gt;"]**
and **--daemon**, Emacs detaches from the terminal and runs fully in the background.
Typically **--fg-daemon["&lt;server name&gt;"]** is used for service launchers like **launchctl**
on MacOS and **systemctl** on Linux

The emacs server can also be started using brew services if this was used to install emacs.
Here emacs-plus@29 emacs version is started with home brow:

> **brew services start emacs-plus@29**
