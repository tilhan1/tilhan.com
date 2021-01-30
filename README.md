# bahadirdogru.com My Personal Blog.

# Based on Memoirs Jekyll Theme

[Live Demo](https://wowthemesnet.github.io/jekyll-theme-memoirs/) | [Docs & Download](https://bootstrapstarter.com/bootstrap-templates/jekyll-theme-memoirs/) |  [Buy me a coffee](https://www.wowthemes.net/donate/)

![memoirs](https://bootstrapstarter.com/assets/img/themes/memoirs-jekyll.jpg)

# How to use

Version: Bootstrap 4

##### A minimalist Jekyll theme built with Bootstrap 4, for blogging purposes. Trendy, modern design, for people who love the beauty of simplicity.

##### Memoirs is a responsive Jekyll Bootstrap Theme, compatible with Bootstrap 4, free for personal and commercial use.

"Memoirs" is a free Bootstrap Jekyll theme for blogging, collections, resources, reviews websites
=================================================================================================

#### Features

-   Built for Jekyll
-   Compatible with Github pages
-   Index Pagination
-   SEO
-   Feed
-   Prism Highlighter
-   Sitemap
-   Post Share
-   Post Categories
-   Related Posts
-   Category Archives (Compatible with Github pages)
-   Post Reviews with Stars
-   Blurred Spoilers
-   Table of Content
-   Lazy Load Images
-   Figure Images
-   Integrations:
    -   Disqus Comments
    -   Google Analaytics
    -   Mailchimp Integration
    -   Adsense
    -   Contact
-   Design Features:
    -   Bootstrap v4.x
    -   Font Awesome
-   Layouts:
    -   Default
    -   Post
    -   Page
    -   Archive
    -   Categories (for 100% compatibility with Github pages)

#### What's Jekyll

If you aren't familiar with Jekyll yet, you should know that it is a static site generator. It will transform your plain text into static websites and blogs. No more databases, slow loading websites, risk of being hacked...just your content. And not only that, with Jekyll you get free hosting with GitHub Pages! If you are a beginner we recommend you start with [Jekyll's Docs](https://jekyllrb.com/docs/installation/). Now, if you know how to use Jekyll, let's move on to using this theme in Jekyll:

#### How to use "Memoirs" theme

-   [Download](https://github.com/wowthemesnet/jekyll-theme-memoirs/archive/master.zip) or `git clone https://github.com/wowthemesnet/jekyll-theme-memoirs.git`

From the rood of your downloaded/cloned folder, open your terminal and install:

```
gem install bundler

```

Cmd

Copy

Then:

```
bundle install

```

Cmd

Copy

Edit `_config.yml` options. If your site is in root: `baseurl: ''`. Also, change your Google Analytics code, disqus username, authors, Mailchimp list etc.

Again, from your terminal:

```
bundle exec jekyll serve --watch

```

Cmd

Copy

You should be able to see your Jekyll project now, if you didn't change the folder name you should see it live at `http://127.0.0.1:4000/jekyll-theme-memoirs`.

Start populating your blog by adding your `.md` files in `_posts`. Memoirs already has a few examples.

YAML front matter options:

-   post image - `image: assets/images/mypic.jpg`
-   external post image - `image: "https://externalwebsite.com/image4.jpg"`
-   disable page comments - `comments:false`
-   meta description (optional) - `description: "this is my meta description"`

##### YAML Post Example:

```
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Lifestyle, Travel ]
tags: [ France ]
image: assets/images/5.jpg
description: "Something about this post here"
---

```

Mardown

Copy

##### YAML Page Example

```
---
layout: page
title: About Memoirs
comments: false
---

```

Markdown

Copy

##### Rating

```
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/5.jpg
description: "Something about this post here"
rating: 4.5
---

```

Markdown

Copy

[Rating Post Demo](https://wowthemesnet.github.io/jekyll-theme-memoirs/review-oscar/)

##### Adsense

Enable this option by editing `_config.yml`.

```
# Adsense (change to "enabled" to activate, also your client id and ad slot. Create a new ad unit from your Adsense account to get the slot.)
adsense: "disabled"
adsense-data-ad-client: "ca-pub-3412143450191416"
adsense-data-ad-slot: "1363087678"

```

Markdown

Copy

##### Lazy Load Images

Enable this option by editing `_config.yml`.

```
# Lazy Images ("enabled" or "disabled")
lazyimages: "enabled"

```

Markdown

Copy

##### Table of Contents

Add `toc:true` on your post YAML.

```
---
layout: post
title:  "Education must also train one for quick, resolute and effective thinking."
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/3.jpg
beforetoc: "Markdown editor is a very powerful thing. In this article I'm going to show you what you can actually do with it, some tricks and tips while editing your post."
toc: true
---

```

Markdown

Copy

`beforetoc` adds a paragraph before the TOC is displayed.

##### Editing stylesheet

You'll only work with a single file to edit/add theme style: `assets/css/theme.scss`.