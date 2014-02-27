---
layout: post
title: "Blurring things with Javascript"
date: 2014-02-26 15:11:18 -0800
comments: true
categories: 
 - webdev
 - frontend
 - programming
---

Recently I was investigating different Javascript libraries for blurring things on mobile. In this case, blurring would act to obscure an image from the user.

<h3><a href="http://blurjs.com/?bg=1">Blur.js</a></h3>
Pros:
<ul>
<li>It's easy; plug and play. It also supports draggable elements (<a href="http://blurjs.com/simpledemo.html">and has a neat demo proving it</a>)</li>
<li>You can specify your overlay color and blur radius, and it even supports caching.</li>
<li>More hackproof; since (on first glance) it seems to replace your original image entirely, you can't easily unblur it using developer tools.</li>
</ul>

Cons:
<ul>
<li>When I used this library for a div with a background-image, the entire image wasn't blurred out; only part of it. It didn't play nicely with my background-image having a <code>background-size:cover</code> style.</li>
<li>Doesn't seem to work for blurring text or colored divs; just elements with some image aspect.</li>
<li>You need to provide a "source" of blurring for some reason.</li>
</ul>

<h3><a href="http://nbartlomiej.github.io/foggy/">Foggy</a></h3>
Pros:
<ul>
<li>Uses the CSS "filter" and falls back to a "manual blur" if the browser doesn't support it.</li>
<li><em>Really</em> simple; at the most basic level, all you need is <code>$(".selector").foggy()</code></li>
<li>It worked on mobile Safari! (And I haven't yet tested it with anything else.)</li>
<li>You can also unblur blurred objects!</li>
</ul>

Cons:
<ul>
<li>The manual blur creates duplicates of elements, so it could be pretty expensive? Especially for a mobile web app, my specific use case. (In my brief tests, I didn't notice any particular behavior downgrade.)</li>
<li>You could "hack" this by inspecting elements to see what the original image is.</li>
</ul>

I ended up using Foggy so that I could grab multiple elements with one selector to blur (rather than needing to iterate through each and supply each one with its own "source"). Also, "hacking" via a developer tool is less of a risk. and, honestly, it just worked more quickly, though I do love the layout of Blur's page better.
