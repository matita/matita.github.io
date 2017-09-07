---
layout: post
title: "Create your first Git repository"
published: false
---

> _If you already know what Git and GitHub are and just want to set up a repository, then you can [skip the intro](#install-git) and jump directly to the [instructions](#install-git)._

Let's say you're a beginner developer, or at least you didn't work with any professional team yet.  
You somehow overheard about Git and/or GitHub but never bothered researching what they are and how they can help you.  
So you could have a question on your mind, before deciding if it's the case to start learning what it is and how to use it:

## Do I really need Git?

If you don't know any other SCM, or don't even know what SCM means, then there is only one valid answer: **YES**.

I can give you just a few reasons that should convince you to use it, especially if paired with an online repository like [GitHub](https://github.com/) or [BitBucket](https://bitbucket.org/):

* **versioning**: did you ever save files with names like _project_v1.cs_, _project_v2.cs_, _project_FINAL.cs_, _project_truly_FINAL.cs_? With Git you don't need to do it anymore, its main purpose is keeping the history of all the files in your project so you just save a **project.cs** file and you can easily restore any previous version whenever you do mistakes and want to revert your changes
* **backup**: when paired with an online service, you can upload your code on their server, so should anything bad happen to your computer or hard-disk, you have an online backup copy of your code that you can download every time you want
* **multiple computers**: if you have different computers where you program it is very easy to sync them with Git
* **code sharing**: it makes easy to make other people view your code, whenever you need help on something that's not working or for any other reason
* **collaboration**: do you have projects you're working on with other people? Are you a game developer and you want to join a jam with a team? Git is the best way to have different people working on the same files without the risk of completely override others' edits
* **quick**: it literally takes no more than 5 minutes to set up a repository after the one-time requirements install, both locally and remotely, so there's nothing stopping you to use it in all your projects
* **universal**: it works with every programming language or every kind of project, it unveils its strenghts with text-based files, but nothing stops you to use it also for images, assets or any kind of binary files (as long as they are not huge)
* **free**: you can surely use Git for free, you can have unlimited open source repositories on GitHub for free and unlimited private repositories on BitBucket if you're working with 5 people or less for free, so definitely money is not a reason to not use it
* last but not least, this is what professional developers use in their day-by-day job, so if you plan to ever have a developer career you better start learning it as soon as possible, so when in the next job interview they'll ask you if you can use Git you'll proudly answer: YES

_Most of these points are valid for any kind of SCM ([Source Control Managers](https://en.wikipedia.org/wiki/Source_control_management)) but Git is the [most popular one](https://rhodecode.com/insights/version-control-systems-2016) and definitely trending.  
Whether Git is better than SVN, Perforce, Mercurial or others is out of the scope of this post._

So, did I convince you to give Git a shot?  
Here below you'll find the instructions to start working with Git in a basic way.  
Don't be scared about the number of steps, you have to do most of them only once, then for each project you want to add the process we'll be very quick, as I promised.


<a name="install-git"></a>

## Install Git on your computer (one-time)

The first thing you have to do is install Git on your machine, so:

1. Head to [https://git-scm.com/](https://git-scm.com/)
2. Download the installer for your platform
3. Execute the installer
4. If you are on Windows I recommend to select the following options when prompted by the installer (the other options can be left on their default):  
    1. **Use Windows' default console window**
    2. **Use Git from the Windows Command Prompt**
    3. **Checkout Windows-style, commit Unix-style line endings**
5. Done! You now have Git installed on your machine

## Create GitHub account (one-time)

1. Head to [https://github.com/join](https://github.com/join)
2. Compile the sign up form and click on **Create an account**
3. In **Choose your plan** step select **Unlimited public repositories for free** and click on **Continue**
4. You can decide to skip the step **Tailor your experience** by clicking **Skip this step** next to _Submit_ button
5. Wait for the email from GitHub to arrive in your inbox and click the **Verify email address** link in it
5. Done! You now have a GitHub account

## Install GitHub Desktop (one-time)

Many developers use Git via a command prompt, but for the sake of this post I'm trying GitHub desktop and I find it very clean, simple and straightforward to use it.  
Plus, despite the name, you can use it for any Git repository, even if they are not on GitHub.



## Create remote repository

## Create local repository

## Upload your files (git push)