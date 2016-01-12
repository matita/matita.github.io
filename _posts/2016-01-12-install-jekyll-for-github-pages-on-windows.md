---
layout: post
published: true
title: Install Jekyll for GitHub Pages on Windows
tags: "github pages, jekyll, windows"
---



Recently I needed to install Jekyll on my Windows computer, mostly for a project I'm working on using GitHub Pages.  
It was not necessary, but testing the development locally is always better and faster than editing some file, git add-git commit-git push and wait for GitHub Pages to render the website.

It seems like installing Jekyll on Windows is not that easy, but following [Nathan Totten's instructions](https://ntotten.com/2012/03/02/github-pages-with-jekyll-local-development-on-windows/) it turned out to be very simple.

I needed it specifically to be compatible with GitHub Pages and my first try at following the instructions were not (currently the latest version of Jekyll is 3.0.1 and GitHub Pages Jekyll is 2.4.0, as seen in [GitHub Pages dependencies page](https://pages.github.com/versions/)).

So here are the few steps I made:


## 1. Install Ruby

Go to [Ruby downloads page](http://rubyinstaller.org/downloads/), download the desired installer under "Rubyinstallers" section (mine was Ruby 2.2.3 x64) and execute it, remembering to check the options: 

* Install Tcl/Tk support
* Add Ruby executables to your PATH
* Associate .rb and .rbw files with this Ruby installation


## 2. Install the Development Kit

In the same [Ruby downloads page](http://rubyinstaller.org/downloads/) download the right Development Kit under the section "Other Useful Downloads / Development Kit" (mine was **For use with Ruby 2.0 and above (x64 - 64bits only)**), execute it and extract it in a folder (for me **C:\DevKit**).

Open a command line in **C:\DevKit** (or where you extracted the Development Kit) and execute the commands:

```
ruby dk.rb init
ruby dk.rb install
```
  
The first time I executed the `install` command it gave me the error `Invalid configuration or no Rubies listed. Please fix 'config.yml' and rerun 'ruby dk.rb install'`, so I edited `C:\DevKit\config.yml` by putting the folder where I had installed Ruby, so the file is now like this (excluding the comments):

```
---
- C:/Ruby22-x64
```

and reran `ruby dk.rb install`.


## 3. Install Jekyll for GitHub Pages

As I said earlier the Jekyll version has to be compatible with GitHub Pages' Jekyll, and GitHub made a proper Ruby gem with all the dependencies needed, like they say in their page about [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/).

I first tried the Bundler approach but it gave me some error, so I created a file named `Gemfile` in the root directory of the repository I needed with this content:

``` javascript
source 'https://rubygems.org'
gem 'github-pages'
```

Then run `gem install github-pages` in the command line and the correct Jekyll version with all its dependencies is installed.


## 4. Ignore unnecessary files in `.gitignore`

To avoid unnecessary file exchange when pushing or pulling from git, edit the `.gitignore` file in the root directory of your repository by appending these lines:

````
Gemfile
_site
```

The `_site` folder is where Jekyll outputs the rendered files, it is unnecessary (maybe dangerous?) to have git sync that folder with GitHub since GitHub Pages renders the site itself.


## 5. You're ready to go!

Just open a command line in the root folder of your repository and run `jekyll serve`: Jekyll will build the website and will serve it on a light web server at `http://localhost:4000/name-of-repository/`. It will also watch for any change in your files and rebuild it without the need of stop/rerun the `jekyll serve` command.
