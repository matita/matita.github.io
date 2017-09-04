---
layout: post
title: "Hosting static html on GitHub Pages for Game Developers"
published: false
---


Recently a friend of mine asked me how to host html pages for a project he's working on using [AirConsole](https://www.airconsole.com/).  
Obviously I suggested the same thing I always suggest in similar occasions: do you need a server where you can host html pages, that you don't have to pay since you're only doing some experiments and you need to have full control on the code you are publishing?  
Easy answer: [GitHub Pages](https://pages.github.com/).

## What is GitHub Pages?

I assume you already know [GitHub](https://github.com/).  
In case you don't (shame on you) we can say that it is a repository where you can share the code of your projects.  
If your project consists of HTML, JavaScript and CSS, GitHub gives us the possibility to render this code in a fully functional website, using the GitHub Pages feature.
Your project website will be accessible via an URL like this: `https://{your-github-username}.github.io/{your-project-name}/`.

Ok, enough with the intro, let's start the path that will allow you to use this magic!

## Instructions

The process may look a bit lengthy, but if you already are a GitHub and Git user you should already be confident with most of the concepts and you could skip most of the steps.

If you are not, you better start learning, since knowing how to use source control is mandatory in a professional development environment, so it's a good chance to learn and fiddle with concepts you don't know very well.

## Create a GitHub account

If you're a developer, chances are you already have a GitHub account.  
If this is the case you can skip this and go to the next step.  
If you don't have it it's high time you create it, it's almost necessary nowadays for a developer career.

One reason that could be of interest for you if you are a Unity developer, apart from hosting HTML pages as explained in this post, is that [Unity Collaborate](https://unity3d.com/unity/features/collaborate) is now part of [Unity Teams](https://unity3d.com/teams) and it means it won't be free anymore starting from October 2017, maybe I'll write a post on how to use git to collaborate with others with Unity projects.

Ok, back to GitHub account creation:

1. Head to [https://github.com/](https://github.com/)
2. Compile the sign up form. Remember that the username you'll choose will be part of the URL of the website, so choose it wisely ;)

## Install Git

In order to use GitHub you better have Git installed on your machine, so:

1. Head to [https://git-scm.com/](https://git-scm.com/)
2. Download the installer for your platform
3. Execute the installer
4. If you are on Windows I recommend to select the following options when prompted by the installer:  
    1. **Use Windows' default console window**
    2. **Use Git from the Windows Command Prompt**
    3. **Checkout Windows-style, commit Unix-style line endings**

## Create the GitHub repository

1. Log in [https://github.com](https://github.com)
2. Click on the `+` button in the upper right corner of the page and select **New repository**
3. Type the name of your project (for example `ghpages-example`) and leave all the other settings as they are by default
4. Click on the **Create repository** button below the form

## Upload your html files to GitHub repository

1. On your computer open a command line 