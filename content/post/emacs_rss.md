+++
title = "Elfeed: Using emacs for reading RSS"
date = 2017-10-12T17:53:00+02:00
lastmod = 2017-10-14T11:43:36+02:00
tags = ["emacs"]
categories = ["emacs"]
draft = false
+++

In last years I have been using Emacs for almost all my daily tasks:

-   Reading my emails (using [mu4e](http://www.djcbsoftware.nl/code/mu/mu4e.html)).
-   Creating the slides for my courses using org-beamer.
-   Using dired to navigate for the file system).
-   Publishing this blog (using [Hugo](https://gohugo.io/) and [ox-hugo](https://ox-hugo.scripter.co)).

The last thing to integrate into emacs is reading blogs and news from RSS files.
Adding [elfeed](https://github.com/skeeto/elfeed) and [elfeed-org](https://github.com/remyhonig/elfeed-org) I was able to create RSS. elfeed-org
is very simple, it allows to add the feeds as items in org-mode:

```text
- Blogs                                                              :elfeed:

  - https://www.meneame.net/rss                                  :news:portada:
  - https://www.meneame.net/rss?status=queued                            :news:
  - http://planet.emacsen.org/atom.xml                                :emacs:
  - https://www.reddit.com/r/programming/.rss                     :programming:
  ...
```

The tags for each feed will be shared for all articles.

Then, loading **elfeed**, it can be obtained a screen showing the different articles:

{{<figure src="/screen/elfeed.png">}}

And selecting an article, it can be open, read and open each link by the default browser.

{{<figure src="/screen/elfeed2.png">}}

Several opinions about elfeed:

-   It is very simple to use.

-   The use of tags is very powerful, not only they received the tags from the
    category, and you can add a tag to an article.

-   The search filter is simple and very powerful, you can filter both for date and for tags.

-   The search filter can be kept as bookmark, so using C-x r b it can be seen the
    article using a particular filter.

To summary, **elfeed** has been a great discovery. If you use emacs, give it a try.
