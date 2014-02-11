---
layout: post
title: "Developing for Opera Mini"
date: 2014-01-21 10:38:15 -0800
comments: true
categories: 
 - webdev
 - mobiledev
---

It came to my attention recently that not only are the majority of the users for one of my projects using Opera Mini, but that Opera Mini has a Very Special way of dealing with Javascript.

From <a href="http://dev.opera.com/articles/view/opera-mini-web-content-authoring-guidelines/#javascript">their authoring guidelines</a>:

<blockquote>
while Mini supports JavaScript just as well as Opera Desktop, interactivity is somewhat more limited. When the user clicks a link or a button, then the Mini client sends that information back to the server, where the server performs the associated action (such as loading a new page, executing some JavaScript, etc.).
<br/><br/>
For authors, the upshot of all this is that once a page has been rendered by the server, it won't change until the user does something on that and there is no way for scripts to run in the background. The user must do something to make Mini talk to the server in order for JavaScript to be unpaused. As a result, you cannot expect things like JavaScript animations or timed Ajax updates to work in the background as they would on a desktop browser.
<br/><br/>
JavaScript running on the Mini server will only run for a couple of seconds before pausing, for resource constraint reasons. This applies to JavaScript run due to an event firing e.g. onload, as well as code run because of a user action.</blockquote>

I'm still working on getting it properly working, which seems impossible given the bulk of Javascript used in this case and its heavy reliance on Ajax.
