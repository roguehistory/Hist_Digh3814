---
title: "Static Websites"
description: "Building a fast and secure site"
date: 2020-01-28T00:10:09+09:00
draft: false
weight: -1
---

Building a website from scratch can be onerous. Using a system like Wordpress or Squarespace etc can leave you locked in to someone else's platform (and any security issues that might entail).

Here, we're going to build a simple website that uses nothing but text files as its source; these text files will always be readable into the future, and you can also copy them to your own machine so that they're always handy, ready to be transformed into something else.

I'm talking about _static site building_; there are many different generators out there that will take your text files, pump them through some templates, and spit out flat html on the other side. At The Programming Historian, there is a lesson by Amanda Visconti on using [Jekyll and Github Pages](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages) to make a site; we're going to do something much easier.

In essence, you are going to create a new repository in your Github account called `your-username.github.io` and it will be set to `public` when you make it; initialize with a `readme.md`. Then, add a new file in there called `index.md` and you're going to write something in that file, eg,

```
## My Quick Static Site

This is a site I build with gh-pages. **Wow**

It reads [markdown](https://www.markdownguide.org/) and turns it into html.

![gif ftw](https://media.giphy.com/media/nXxOjZrbnbRxS/200w_d.gif)
```

Commit that file. Then, hit the gear wheel icon (the settings) and scroll down to the Github Pages section. Github will run your text files through the Jekyll site builder for you; here you can select from some of their templates.

Boom! [The full process is on this site with screenshots](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site).

## Content

Now, consider how you want to explain your work so far in this course on the graveyard project. You might want to create some subpages; just make these in your repo as text files ending in `.md`. When Github builds your page, it will add these to the navigation. Put images in the same folder, and then you can link to them with `![al-text describing the image](image-filename.png)` (or .jpg, right? Depends on the filename?).

The layout and so on is probably not going to be perfectly what you want. There will be time enough to fiddle with this, and there are any number of tutorials out there on customizing a gh-pages simple site. **Don't worry about that right now**. Think of your content first, for this week.

## Going Further

Now, there's a lot more to static websites than this. This course site is generated with [Hugo](https://gohugo.io); a site generator for building exhibitions, called 'Wax', is available [here](https://minicomp.github.io/wax/). (Speaking of exhibits, here's information about building them with [Omeka.net](https://programminghistorian.org/en/lessons/up-and-running-with-omeka).)
