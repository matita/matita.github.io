---
layout: post
published: false
title: Jekyll errors for GitHub Pages update to Jekyll 3.0
---


Quite recently [GitHub Pages updated to Jekyll 3.0](https://github.com/blog/2100-github-pages-now-faster-and-simpler-with-jekyll-3-0). As every migration it could bring to some issues, so here are my findings for a project that I'm working on.

Since it is not a basic blog but a bit more complex project, I suspect I will find some more issues. I'm writing those as soon as I'll find them.

## `relative_permalinks` compatibility

I started to acknowledge it before the announcement since some warning about the compatibility with Jekyll 3.0 of `relative_permalinks` configuration in `_config.yml`.

This was easy: I just removed the `relative_permalinks` clause in the config file and the problem disappeared.

## Missing dependency: kramdown

But, after the announcement, I couldn't build anymore the site for a project I am working on, so I `git pull`ed, updated my local project dependencies with `gem update github-pages` and tried to `jekyll serve`.

It gave me an error of `missing dependency: kramdown`, so asking Google how should I resolve this and it told me to `gem install kramdown` or add `gem 'kramdown'` to the `Gemfile`. This didn't work for me.

After some other searches I found the solution in [this post from Tom Elliot](http://telliott.io/2015/07/27/how-i-broke-jekyll-with-my-gemfile.html). Basically now I just have a `Gemfile` made like this:

```
source 'https://rubygems.org'
gem 'github-pages'
```

and running

```
bundle clean --force
bundle install
```

resolved my issue.

## Stack level too deep exception

I thought it was all good! But I was wrong...

When I ran `jekyll serve` it gave me a `stack level too deep exception in _layout/post.html`.

Again Google gave me some hint by pointing me at [an issue](https://github.com/jekyll/jekyll/issues/3207) on Jekyll GitHub repository.

I searched for all the occurences of `jsonify` in my templates and I found I was using `var post = {{ page | jsonify }};`.

I tried to replace it with `var post = {{ page }};` and so I could `jekyll serve` without errors.

Unfortunately this would not work for me since the output of `{{ page }}` is obviously not a valid json, so I had to replace that row in my template with this:

``` javascript
var post = {
	title   : {% raw %}{{ page.title | jsonify }}{% endraw %},
    path    : {% raw %}{{ page.path | jsonify }}{% endraw %},
    content : {% raw %}{{ page.content | jsonify }}{% endraw %}
};
```

I don't like this solution very much, but it works for now since currently I only need these properties for the rendered post. If I'll come up with a better solution I'll write about this.