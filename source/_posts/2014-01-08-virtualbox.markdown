---
layout: post
title: "Running IE7, IE8, and IE9 on a Mac, Using VirtualBox"
date: 2014-01-08 09:07:20 -0800
comments: true
categories: [webdev]
---

I've been putting off getting a virtual machine running on the Mac computer I use for work, mostly because I wanted to forget the existence of <IE9 browsers entirely. Unfortunately, the visual bugs accumulating across my projects were starting to get a little ridiculous.

<img class="book-cover" src="{{ root_url}}/images/proleft.png" alt="Screenshot of IE8 errors"/>
<p class="caption">omg why</p>

After some hours of searching and fiddling, I discovered my favorite solution for running IE on a Mac. It goes like this:

<ol>
<li>Download the relevant/recent version of Oracle's <a href="http://www.virtualbox.org">VirtualBox</a>.</li>
<li>Use the Terminal and and run <code>curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | env IEVMS_VERSIONS="8 9" bash</code> to download 2 virtual machines; one that can run IE8, and one that can run IE9.</li>
</ol>

That's it! Once that's finished, you can open VirtualBox and you'll see your boxes all ready to go.

<img class="book-cover" src="{{ root_url}}/images/virtualbox.png" alt="Screenshot of IE8 in VirtualBox"/>
<p class="caption">only IE8 is pictured above</p>

Thanks to <a href="http://osxdaily.com/2011/09/04/internet-explorer-for-mac-ie7-ie8-ie-9-free/">OSXDaily</a> for the post that led me to finding <a href="https://github.com/xdissent">xdissent</a>'s awesome installations.

Other notes:
<ul>
<li><code>border-radius</code>, <code>rem</code>, and <code>opacity</code> are some of the many words not recognized by IE8.</li>
<li>PressF12 to open up IE8's Developer Tools.</li>
</ul>
