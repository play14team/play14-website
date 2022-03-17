---
layout: post
title: Welcome to our new website
date: 2016-12-08 22:47:05
categories:
  - Announcement
tags:
  - website
author: Cédric Pontet

excerpt: Announcing our brand new website, powered by Jekyll, hosted on GitHub Pages.

images:
  - /images/play14_500x500_black_bg.png

enableComments: true
---

Our brand new **#play14** website is awesome, fully responsive and fast.  
It will allow us to provide more content, like

- general information about **#play14**
- descriptions of games
- history of all the passed **#play14** events
- blog posts, to give some news and povide any realted content

---

#### Technology

This website is powered by [Jekyll](https://jekyllrb.com) and hosted on [GitHub Pages](https://pages.github.com/).  
You can find the source code on our [GitHub repository](https://github.com/play14team/play14-website)

---

#### Work in progress

The site is currently a work in progress.  
So bear with us while we are still working on it. Don't hesitate to give us a shout if you notice something that doesn't work.

---

#### Providing content

You can start providing content by creating a [pull request](https://yangsu.github.io/pull-request-tutorial/) on our [GitHub repository](https://github.com/play14team/play14-website).

Blog posts, Games and Events are all describes in [Markdown](https://daringfireball.net/projects/markdown/) using Jekyll's [YAML Front Matter](https://jekyllrb.com/docs/frontmatter/).  
You can find more information on how to write a blog post with Jekyll [here](https://jekyllrb.com/docs/posts/).

Directory structure

- Events markdown files should be placed into the `_events` directory.
  - The file name should respect the template `<yyyy-mm>.md`.
  - Events images should be placed into the `images/events/<event-name>` sub-directory. Their size should be 600x500.
- Games markdown files should be placed into the `_games` directory.
  - The file name should respect the template `<game-name>.md`.
  - Game images should be placed into the `images/games/<game-name>` sub-directory. Their size should be 800x533.
  - Game files should be placed into the `files/<game-name>` sub-directory.
- Posts markdown files should be placed into the `_posts` directory.
  - The file name should respect the template `<yyyy-mm-dd-post-title>.md`.
  - Post images should be placed into the `images/posts` sub-directory. Their size should be 800x533.
