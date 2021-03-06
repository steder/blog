---
layout: post
title: "Starcraft Emacs Mode (Or How to make an Emacs Minor-mode)"
date: 2012-04-29
comments: false
---

<div class='post'>
    A friend of mine once said that he was terrible at Starcraft because his "<a
        href="http://www.youtube.com/watch?v=YbpCLqryN-Q">APM</a>" was too low. &nbsp;APM, if you're not familiar with
    the acronym stands for &nbsp;"Actions Per Minute" and refers to keypresses or mouse clicks per minute while playing
    the RTS turned sport, Starcraft. <br />
    <div><br /></div>
    <div>My friend continued saying that he actually thought his APM while programming was quite high, certainly higher
        than anything he could manage playing Starcraft. &nbsp;Of course, having nothing better to, I hacked up an Emacs
        minor mode that would track all your key presses within Emacs and total up an APM score for you.</div>
    <div><br />
        <table cellpadding="0" cellspacing="0" class="tr-caption-container"
            style="float: left; margin-right: 1em; text-align: left;">
            <tbody>
                <tr>
                    <td style="text-align: center;"><a
                            href="/images/emacs-starcraft.png"
                            imageanchor="1"
                            style="clear: left; margin-bottom: 1em; margin-left: auto; margin-right: auto;"><img
                                border="0" height="65"
                                src="/images/emacs-starcraft.png"
                                width="640" /></a></td>
                </tr>
                <tr>
                    <td class="tr-caption" style="text-align: center;">starcraft.el in 'action'</td>
                </tr>
            </tbody>
        </table><br /><br /><br /><br />Yes, that "sc" in the modeline stands for Starcraft. &nbsp;Install starcraft.el
        in your emacs configuration and find how hard it is to inflate your actions per minute while writing code in
        emacs compared to spaming hotkeys in Starcraft 2.<br /><br />Really, I just wanted to do a more substantive bit
        of Emacs Lisp and this was a fun excuse to do so. <br /><br />You can download and play with the mode <a
            href="https://gist.github.com/1990900">here</a> on <a href="https://gist.github.com/1990900">Github</a>.
        <br /><br />
    </div>
</div>
<h2>Comments</h2>
<div class='comments'>
    <div class='comment'>
        <div class='author'>Andrew</div>
        <div class='content'>
            Nice. I think I will install this as a &quot;productivity measuring tool&quot; for all my developers.</div>
    </div>
</div>