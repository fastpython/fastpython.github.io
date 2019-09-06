---
layout: page
title: How?
permalink: /how/
categories: start-with-this
---


# How is this blog created

Content of the blog comes from lessons learned while developing software with Python for web. One of the good tips to give is how this blog is generated. 

Blog is built using [MkDocs](https://www.mkdocs.org/) and hosted on [Github Pages](https://pages.github.com/). MkDocs is a fast and simple static site generator that's geared towards building project documentation. The theme is [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). With MkDocs all site content is written in Markdown and pages configured with a single YAML configuration file.

Even though MkDocs is meant for project documentation it's very good alternative for tech blogs as well. Especially when you combine it with Github Pages.

- It's free. 
- You can use markdown. 
- Need only text editor. 
- Use Git for version control. 
- Lightweight process (_write, commit, push_)

Combination of MkDocs and Github Pages is very easy to like if you are a software developer by profession. Not to forget that MkDocs is of course [developed with Python](https://github.com/mkdocs/mkdocs/).


<div style="text-align:center; margin-top: 3em; margin-bottom: 3em;">
    <a href="https://squidfunk.github.io/mkdocs-material/">
        <img src="/img/mkdocs-material-theme.png" title="MkDocs Material">
    </a>
</div>


## How to get started

To get started you need to first install MkDocs. [Documentation](https://www.mkdocs.org/) has good instructions for that. To sum it up, it'll look like this:

```
$ pip install --upgrade pip

$ pip install mkdocs

$ mkdocs --version
mkdocs, version 1.0.4 from /site-packages/mkdocs (Python 3.7)
```

When MkDocs is up and running you can start you brand new blow with:

```
$ mkdocs new the-blog

$ cd the-blog

$ mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 190809 22:28:54 server:296] Serving on http://127.0.0.1:8000
[I 190809 22:28:54 handlers:62] Start watching changes
[I 190809 22:28:54 handlers:64] Start detecting changes
```

Open up `http://127.0.0.1:8000/` in your browser, and you'll see the default MkDocs home page being displayed. Stop the server with `Ctrl-C`. If the theme is not for you, you can try the material them used in this blog. The easiest option to get started with the theme is to clone the repository and start tweaking from there.

```
$ cd ..

$ git clone https://github.com/squidfunk/mkdocs-material.git

$ cd mkdocs-material

$ mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 190809 22:28:54 server:296] Serving on http://127.0.0.1:8000
[I 190809 22:28:54 handlers:62] Start watching changes
[I 190809 22:28:54 handlers:64] Start detecting changes
```

Open up `http://127.0.0.1:8000/` in your browser again. Now just to browse through the [mkdocs-material](https://squidfunk.github.io/mkdocs-material/getting-started/) pages.


## Deploy to Github

Github pages has few options on how you can commit your files and be served as static pages. For personal blog the easiest option is to use Project page style and commit served static site on `master` branch. Detailed instructions for doing it can be found from [MkDocs documentation](https://www.mkdocs.org/user-guide/deploying-your-docs/#github-pages) and from [Github pages documentation](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages).

With MkDocs it'll be as easy as command below assuming you'll want to publish using master branch. 

```
$ mkdocs gh-deploy -b master
```

Whatever branch you use, don't ignore the warning that MkDocs documentation gives you.

> Warning
> 
> You should never edit files in your pages repository by hand if you're using the `gh-deploy` command because you will lose your work the next time you run the command.

On other words it means that you should not edit any files in _the deploy branch_, i.e. `master`. Deploy command will change them. Good method of working is to write your blog in e.g. `blog` branch. Commit all changes to `blog` branch and deploy using `master`. Github pages allow also using `gh-pages`, but there are limits and using `master` is support in all different cases.


<div style="margin-top: 8em;"></div>
