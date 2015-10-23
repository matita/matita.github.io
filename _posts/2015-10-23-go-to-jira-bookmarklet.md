---
layout: post
published: true
title: Go to JIRA bookmarklet
---

Premise: I love bookmarklets. They allow to execute a piece of code even without a browser plugin installed. You as a user have complete control on when to execute the code, not like the browser plugins that could execute code for every single page you visit. You don't have to install them, just drag'n'drop to the bookmarks bar, or delete them whenever you want.

This to say that every time I need a feature for the browser that's not built-in, I always try to make a bookmarklet and see what I can do to make my daily work better.

This time I had this problem: in the company where I work we use JIRA as a bug tracker. Actually we use more than one on different servers/domains/locations since we have partners that use their own JIRA installation. It's not unusual to send or receive emails with the ID of the JIRA issue (e.g. PROJ-662) but without a link, and it's always a pain to remember which JIRA server the projects relates to, point the browser to that page, then search the issue number (I know it's not that difficult, but I'm a developer: I'm lazy).

What I really wanted was to select the issue ID and click something that redirected me directly to the correct URL. Guess what? Yeah, I made a bookmarklet to do exactly this.

You can find it [here](http://matita.github.io/gotojira-bookmarklet/).

Just fill the form with the projects short names (the first part of an issue ID) and the URL of where the related JIRA installation is, then drag the the bookmarklet on your bookmarks bar and you're done!

Don't worry, it's everything client side and I won't track your super secret JIRA locations. If you don't trust me you can see it by yourself in the source code on [GitHub](https://github.com/matita/gotojira-bookmarklet).

When you select an issue ID and click on the bookmarklet you're automagically redirected to the correct JIRA page.

If you click the bookmarklet with nothing selected you are prompted to insert the issue ID you want to view.

The first project defined is also the default one, i.e. the implicit project if you just put the digits of the ID (e.g. 662 instead of PROJ-662).

**Pro tip:** when you add the projects in the customization form the current URL auto-updates, so you can share your configuration with your colleagues by directing them to the same URL.
