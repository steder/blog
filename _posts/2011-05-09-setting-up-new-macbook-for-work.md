---
layout: post
title: "Setting up a new macbook for work"
date: 2011-05-09
comments: false
---

<div class='post'>
    First day at the new job and I'm setting up a new macbook pro (macbookpro 8,2) for work.<br /><br />Here's a list of
    things I'm doing to setup this machine as a reference for future installations:<br /><br />* Ran "Software
    Update"<br />* Installed XCode (3.x because it's free and is included on your install media) and X11<br />*
    Installed Chrome<br />* Installed Firefox<br />* Installed Opera<br /><br />Break for lunch, frustrating phone call
    with fifth third bank, and reset my MCS account passwords...<br /><br />* After debating using macports, fink, or
    homebrew decided to give homebrew a try.<br />* brew install python (which installs readline, gdbm, and
    python2.7.1).<br />* Added /usr/local/share/python to PATH<br />* easy_install pip<br />* pip install virtualenv
    virtualenvwrapper mercurial<br />* hg clone https://bitbucket.org/steder/dotfiles etc <br />* cd etc &amp;&amp;
    ./setup_links_mac.sh<br />* Added path customizations for homebrew to ~/.bashrc<br />* brew install emacs --cocoa
    --with-x<br />* ln -s /usr/local/Cellar/emacs/23.3/Emacs.app /Applications/<br />* brew install subversion<br />*
    Didn't find grep in the default homebrew (they include system duplicates by default) but apparently you can just
    point homebrew at a recipe on some random site and it'll install it... Not sure I'm happy with this but that's
    probably the reason homebrew runs as a non-root user... Basically you can do: sudo brew install
    https://github.com/adamv/homebrew/raw/duplicates/Library/Formula/grep.rb<br />* generated an ssh key: ssh-keygen -t
    rsa -b 4096<br />* brew install ssh-copy-id<br />* enabled sshd in the sharing control panel<br />* ssh-copy-id
    msteder@localhost<br />* sent authorized keys files to systems guys for setup on the MCS resources.<br />* brew
    install wget<br />* brew install proctools<br />* brew install openssl<br />* Installed Dropbox<br />* Installed
    http://www.levien.com/type/myfonts/inconsolata.html <br /><br />I think that may be just about enough setup for
    today. I'm thinking next steps are going to be installing AWS tools like s3cmd, boto, etc.</div>
<h2>Comments</h2>
<div class='comments'>
    <div class='comment'>
        <div class='author'>Mike</div>
        <div class='content'>
            I&#39;m not sure if this is sarcastic or not. :-) I didn&#39;t expect it myself obviously. And I think if it
            were a more publish or perish driven group I wouldn&#39;t be here. The team here is responsible for
            www.globusonline.org.</div>
    </div>
    <div class='comment'>
        <div class='author'>Michael Tobis</div>
        <div class='content'>
            Back at UC - now there&#39;s a surprise...</div>
    </div>
</div>