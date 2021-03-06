---
layout: post
title: "Emacs 23 On Leopard"
date: 2009-12-21
comments: false
categories:
- emacs
- mac
---

<div class='post'>
    <span style="font-family: 'Lucida Grande'; font-size: small;"><span class="Apple-style-span"
            style="font-size: 11px;"><span class="Apple-style-span"
                style="font-family: Times; font-size: medium;"></span></span></span><br /><span
        style="font-family: 'Lucida Grande'; font-size: small;">Just a quick note on building emacs-cvs (emacs23+) on
        Mac OS 10.6.<br /><br />First, check emacs out:<br /></span><br /><span
        style="font-family: 'Lucida Grande'; font-size: small;"></span><br /><span
        style="font-family: 'Lucida Grande'; font-size: small;"></span><br /><span
        style="font-family: 'Lucida Grande'; font-size: small;">
        <blockquote>$ mkdir Emacs; cd Emacs&nbsp;&nbsp;</blockquote>
        <blockquote>$ cvs -z3 -d:pserver:anonymous@cvs.savannah.gnu.org:/cvsroot/emacs co emacs-cvs</blockquote>Or check
        it out via&nbsp;<a href="http://bazaar.canonical.com/">Bazaar</a>:<br /><br /><br />
        <blockquote>$ bzr branch http://bzr.savannah.gnu.org/r/emacs/trunk emacs-bzr&nbsp;</blockquote>
        <br /><br />&nbsp;Now create a scratch directory:<br />
        <div><span style="font-family: monospace;"><span class="Apple-style-span" style="white-space: pre;">
                </span></span></div>
        <blockquote>$ mkdir emacs-build</blockquote>
        <blockquote>$ cd emacs-build</blockquote><br />To build the mac App bundle of
        emacs:<br /><br /><br /><br /><br />
        <blockquote><br /></blockquote>
        <blockquote>$ ../emacs-cvs/configure --with-ns</blockquote>
        <blockquote>$ make install&nbsp;</blockquote>
        <blockquote>$ open nextstep/Emacs.app # just a test to confirm it works before installing</blockquote>
        <blockquote>$ sudo cp -r src/Emacs.app /Applications</blockquote><br />To build a more old school
        x11/commandline emacs as well as replacing the emacs22 that ships as the<br />default on Snow Leopard.
        &nbsp;This is my preferred install as I tend to stick to the commandline whenever
        possible:<br /><br /><br /><br /><br /><br />
        <blockquote>$ ../emacs-cvs/configure --prefix=/usr --with-x-toolkit=no --with-jpeg=no --with-png=no
            --with-gif=no --with-tiff=no</blockquote>
        <blockquote>$ make</blockquote>
        <blockquote>$&nbsp;./src/emacs -q # just a test to confirm it's working before installing</blockquote>
        <blockquote>$ sudo make install</blockquote>
        <div><br /></div>
    </span><span style="font-family: 'Lucida Grande'; font-size: small;"><br /></span></div>
<h2>Comments</h2>
<div class='comments'>
    <div class='comment'>
        <div class='author'>Mike</div>
        <div class='content'>
            @kds:<br /><br />Sorry for the late reply, I had comment moderation on and no notifications setup so it
            languished for a while. <br /><br />Hopefully you&#39;ve already sorted out your issues but I think
            you&#39;ll want to look into grabbing Fink and installing
            it.<br /><br />http://www.finkproject.org/<br /><br />Then you should be able to do:<br /><br />$ fink
            install ncurses-dev</div>
    </div>
    <div class='comment'>
        <div class='author'>kds</div>
        <div class='content'>
            Under OSX 10.6.5, I get the following:<br />configure: error: I couldn&#39;t find termcap functions (tputs
            and friends).<br />Maybe some development libraries/packages are missing? Try
            installing<br />libncurses-dev(el), libterminfo-dev(el) or similar.<br /><br />Where would I get these?
        </div>
    </div>
    <div class='comment'>
        <div class='author'>Mike</div>
        <div class='content'>
            Ah, just do ./src/emacs -nw.<br /><br />-nw stands for &quot;no window&quot; I think.<br /><br />Hope
            you&#39;re enjoying Emacs!</div>
    </div>
    <div class='comment'>
        <div class='author'>ロレ</div>
        <div class='content'>
            Thanks for this!<br /><br />When I run the generated binary ./src/emacs, it launches a separate X11
            instance. Is there any way to have emacs launch in the Terminal itself?</div>
    </div>
</div>