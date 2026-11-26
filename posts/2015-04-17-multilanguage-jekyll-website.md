---
title: "My own multilanguage Jekyll website"
date: 2015-04-17
tags: ["Programming"]
description: "A very long introduction"
permalink: "/en/multilanguage-jekyll-website/"
---

# A very long introduction

> Jekyll is an open source program, written in Ruby by Tom Preston-Werner,
> GitHub’s co-founder. Jekyll is a simple, blog-aware, static site generator for
> personal, project, or organization sites. Instead of using databases, Jekyll takes
> the content, renders Markdown or Textile and Liquid templates, and produces a
> complete, static website ready to be served by Apache HTTP Server, Nginx or another
> web server. Jekyll is the engine behind GitHub Pages, a GitHub feature that allows
> users to host websites based on their GitHub repositories.
>
> – [Wikipedia](http://en.wikipedia.org/wiki/Jekyll_%28software%29)

Well, that saved me a whole paragraph in this post! Couldn’t really find better words
to describe Jekyll. A really interesting and simple tool to build websites from mere
ASCII files.

> Hey! Like HTML, PHP and Javascript!

Ok, ok, you got me. Indeed, most of web technologies are based on *ASCII* files, apart
from Databases for example. Anyway the beauty of Jekyll is that the ASCII files are
[Markdown](http://en.wikipedia.org/wiki/Markdown) files that follow a minimal set of rules to format text. This rules are
such that the bare ASCII file, without the parsing, is still quite readable. It is
similar to [Wiki Markup](http://en.wikipedia.org/wiki/Help:Wiki_markup).

Jekyll is great, easy to use, even a baby can set it up, it is fast, simple, and generates
custom static pages that can be trimmed down to a minimum if needed. Piece of cake!

However, as always as something related to the web comes into my hands, I found a big
issue: design. I may not be a good designer[1](#fn:1) but I know how a good designs looks like.
Most importantly, I know how I like my website. Thus the first thing I did was to try
to find a suitable design for my minimalistic idea of a blog. Googling around I
stumbled upon a very neat and pretty Jekyll design called [So Simple](http://mmistakes.github.io/so-simple-theme/) from desginer
[Michael Rose](http://mademistakes.com/about/). I fell immediately in love with it and decided that it was going
to be the new Look&Feel for my site.

# Setting up your first Jekyll website

So let’s say you’ve found, like me, a neat, cool and usable theme for Jekyll[2](#fn:2) and you
want to start using it. The first thing you need to do is install Jekyll itself. You can
do that by opening a shell and executing the following lines:

```
$ gem install bundler  # This install the bundler utility that eases dependency solving for Ruby
$ git clone git@github.com:mmistakes/so-simple-theme.git # For the So Simple theme using SSH
$ cd so-simple-theme
$ bundle install # To install the Ruby dependencies specified in the Gemfile file. You may need sudo here.
$ bundle exec jekyll serve  # To serve the website at http://localhost:4000
```

Done! You have your new website up and running in your machine! Go to <http://localhost:4000>
and check it out. Neat, right!? Well, true, nobody can see your website right now, but you do. Play around
and check all the nice things that come with the theme you selected. If you need to stop the server just go
to the shell and Ctrl-C it.

> What hellish jargon is all this **shell**, **sudo**, **git**, **website**??

Oh, wait. I didn’t disclaim that. Let’s do it now:

|  | DISCLAIMER |
| --- | --- |
|  | *This blog is mainly aimed to advanced users and/or/xor developers* |
|  | *with broad experience in Linux-ish systems that have been able to* |
|  | *solve the conundrums of the shell and have suffered early installations* |
|  | *of LInux distros in their flesh. I deny all liability related to a* |
|  | *misunderstanding and/or misuse of the instructions contained in this post.* |
|  | *Besides: [Google](http://www.google.com).* |

I feel better now. Let’s continue. Now that we have a theme on our hands that we can serve
from our own machine, what next? Well, it will depend on your theme of choice, but typically
the first thing you want is to edit the \_config.yml file. This file contains the Jekyll site
configuartion. Things like the Blog’s name, server URL acting as the site host, type of
Markdown languge and other goodies are found here.

Then you typically have the \_posts directory. This one contains the posts for your blog.
Inside this directory you may find some more directories: these are the categories of
your posts. And then inside the posts themselves. There are other interesting directories
at the root level:

* \_layouts - Containing HTML files with the layout of your different pages
* \_includes - Containing some more HTML files that are directly included in other HTML files (things like headers and footers)
* \_data - Containing some valuable YAML data that can be used in your site to customize stuff

All this files, and templates, and layouts, and YAML data are mixed and shaked together and then
compiled into your final site. The most important part here is to change the main menu in the
\_data/navigation.yml file:

```
# Site navigation links

- title: About
  url: /about/

- title: Articles
  url: /articles/

- title: Blog
  url: /blog/

- title: Theme Setup
  url: /theme-setup/

- title: Made Mistakes
  url: http://mademistakes.com

- title: Search
  url: /search/
```

---

http://www.girliemac.com/blog/2013/12/27/wordpress-to-jekyll/

1. Hint: I’m not. [↩](#fnref:1)
2. If you intend to setup a Jekyll site from scratch please follow this [tutorial](http://jekyllrb.com/docs/quickstart/). [↩](#fnref:2)

Please enable JavaScript to view the [comments powered by Disqus.](http://disqus.com/?ref_noscript)
[comments powered by Disqus](http://disqus.com)
