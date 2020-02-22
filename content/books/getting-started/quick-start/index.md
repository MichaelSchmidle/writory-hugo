---
order: 1
title: Quick Start
summary: Get up and running in five simple steps
date: 2020-01-28
resources:
- name: cover
  src: 
---

{{<alert class="wy-alert-info">}}
##### Info

Steps 1 through 3 are pretty much standard for any Hugo theme.
{{</alert>}}

## 1: Create a New Site

Once you have [installed Hugo](https://gohugo.io/getting-started/installing), create a new site. To this end, run the following command from your terminal:

```
hugo new site quickstart
```

This will create the folder structure required for a Hugo website.

## 2: Download Writory Theme

Assuming you are using [Git](https://git-scm.com/) for your website, switch to the themes directory of the newly created site, initialize your git repository, and add the Writory theme as submodule:

```
cd quickstart
git init
git submodule add https://github.com/MichaelSchmidle/hugo-writory-theme/ themes/writory
```

If you don't want to use Git, you also can download the latest release of the Writory theme from [Github](https://github.com/MichaelSchmidle/writory-hugo-theme/releases/). Extract the contents of the archive into the ``themes`` folder of your newly created Hugo site.

## 3: Configure Hugo to Use the Writory Theme

Open the file ``quickstart/config.toml`` and edit or add the following lines:

```
theme = "writory-hugo-theme"

[taxonomies]
author = "authors"
series = "series"
```

Run the command ``hugo server`` in your ``quickstart`` directory, browse to ``http://localhost:1313/`` and you will see your bare Writory site welcoming you!

## 4. Add Your First Content

Take advantage of the built-in archetypes. These are templates for creating Markdown files for your books, chapters, series, and authors.

To create your first book, run the following command in your terminal:

```
hugo new --kind book books/my-first-book
```

This will create the file ``content/books/my-first-book/_index.md`` ready for you to edit. Open it and you will see the following front matter:

```
layout: toc
title: My First Book
authors: []
summary: ""
series: ""
resources:
- name: cover
  src: ""
featured: true
ended: false
draft: true
```

Complete it to your liking. Then add chapters, series and authors by running the following commands in your terminal:

```
hugo new --kind chapter books/my-first-book/my-first-chapter
hugo new --kind series series/my-first-series
hugo new --kind author authors/my-first-author
```

Add your meta data to the front matter of these files and you have your first content! Remember to set ``draft: false`` if you want your new content to be rendered by Hugo.

## 5: Modify Your Homepage

Once you have published your first book, the homepage will show a generic welcome message to your visitors. To provide your own, create an ``_index.md`` file in the ``contents`` folder of your site, then write your own Mardown text.

That's it! You have created your Writory themed site and created your first content. Congratulations!
