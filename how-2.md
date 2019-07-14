---
layout: page
title: How
permalink: /how/
categories: start-with-this
---


# How is this blog created

Content of the blog comes from lessons learned while developing web apps. One of the good tips to give is how this blog is generated. 

Blog is built using [MkDocs](https://www.mkdocs.org/). It's a fast and simple static site generator that's geared towards building project documentation. The theme is [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). The theme is built using Google's [Material](https://material.io/design/) Design guidelines. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

Even though MkDocs is meant for project documentation it's very good alternative for tech blogs as well. 

- It's free. 
- You can use markdown. 
- Need only text editor. 
- Use Git for version control. 
- Lightweight process (_write, commit, done_)
- ... 

Combination of MkDocs and Material theme is very easy to like if you are a software developer by profession. Most importantly its [developed with Python](https://github.com/mkdocs/mkdocs/).


{:refdef: style="text-align: center; margin-top: 40px; margin-bottom: 40px;"}
![MkDocs Material](/assets/img/mkdocs-material-theme.png)
{: refdef}


# How to get started

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

