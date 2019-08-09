---
layout: page
title: How
permalink: /how/
categories: start-with-this
---


# How is this blog created

Content of the blog comes from lessons learned while developing web apps. One of the good tips to give is how this blog is generated. 

Blog is generated using [Jekyll](https://github.com/jekyll/jekyll) and hosted on [Github Pages](https://pages.github.com/). If you feel like writing a blog, Jekyll + Github Pages is an very good alternative. 

- It's free. 
- You can use markdown. 
- Need only text editor. 
- Use Git for version control. 
- Lightweight process (_write, commit, done_)
- ... 

Combination is very easy to like if you are a software developer by profession. Only downside is that it's not Python.


{:refdef: style="text-align: center; margin-top: 40px; margin-bottom: 40px;"}
![Jekyll + Github Pages](/assets/img/jekyll_github.png)
{: refdef}


# How to get started

To get started with Jekyll and Github Pages see following links:

- [Jekyll documentation](https://jekyllrb.com/docs/github-pages/) about Github pages
- [Articles on Github](https://help.github.com/en/articles/using-jekyll-as-a-static-site-generator-with-github-pages) about hosting Jekyll generated site
- Straightforward step-by-step [blog post](https://onextrapixel.com/start-jekyll-blog-github-pages-free/) on how to start Jekyll blog on Github pages

Github Pages is doing lot of stuff for you, so, you don't even need to run Jekyll on your local machine if you don't want to. You could just write, commit and move on. Most likely, however, you want to still preview posts, tweak layout, test stuff, etc. 

So, how to do that?


# Steps to generate the blog

To be able to generate Jekyll blog you need to have `ruby`, `gem` and `jekyll` up and running. If you don't you'll find more instructions from [Ruby](https://www.ruby-lang.org/) and [Jekyll](https://jekyllrb.com/) pages.

You should consider also [github-pages](https://github.com/github/pages-gem) gem.

And, to check that those are all Ok, try something like this:

```
$ ruby -v
ruby 2.3.7p456 (2018-03-28 revision 63024) [universal.x86_64-darwin18]

$ gem -v
2.5.2.3

$ jekyll -v
jekyll 3.8.6
```

To start a new blog follow [Jekyll docs](https://jekyllrb.com/docs/) for starting a new blog. To put it briefly:

```
$ jekyll new this-new-blog
```

When that's all good, you can build the Jekyll blog. Generally Jekyll is very nice tool to use. See the [Command Line Usage](https://jekyllrb.com/docs/usage/) page. You don't often see that simple and good looking guide. 

To build Jekyll blog pages you would run:

```
$ jekyll build
```

However, if you are using Github Pages, you don't need to do that. What you want, is to just preview the pages before commiting changes. You can run test server with:

```
$ jekyll serve
```

It'll open web server and server your blog for you to look at on [http://localhost:4000](http://localhost:4000).


# Theme of the blog

Fast Python blog is using Jekyll theme [mkdocs-jekyll](https://github.com/vsoch/mkdocs-jekyll). As the it's said on themes page its _"The Material theme from MkDocs provided as a Jekyll template, optimized for GitHub Pages"_. 

