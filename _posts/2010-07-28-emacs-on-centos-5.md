---
layout: post
title: "Emacs on Centos 5"
date: 2010-07-28
comments: false
---

<div class='post'>
    Attempting to follow my <a href="http://blog.penzilla.net/2009/12/emacs-23-on-leopard.html">install
        directions</a>&nbsp;on a centos VM I found I was missing a bunch of things. &nbsp;So here's a quick brain dump
    of packages you can install to make emacs compile without too much trouble.<br />
    <ul>
        <li>yum -y groupinstall "Development Tools"</li>
        <li>yum -y install gtk+-devel gtk2-devel</li>
        <li>yum -y install libXpm-devel</li>
        <li>yum -y install libpng-devel</li>
        <li>yum -y install giflib-devel</li>
        <li>yum -y install libtiff-devel libjpeg-devel</li>
        <li>yum -y install ncurses-devel</li>
        <li>yum -y install gpm-devel dbus-devel dbus-glib-devel dbus-python</li>
        <li>yum -y install GConf2-devel pkgconfig</li>
        <li>yum -y install libXft-devel</li>
        <li>cd ~/Emacs/emacs-build</li>
        <li>~/Emacs/emacs-bzr/configure --prefix=/usr/local --without-selinux --with-x-toolkit=gtk</li>
    </ul>
    <div>You may not need to build without selinux, YMMV.</div>
</div>