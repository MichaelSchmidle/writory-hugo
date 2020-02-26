---
order: 3
title: "Navigation"
summary: "Learn How to Create Your Navigation Menu"
date: 2020-02-26
---

## Why Writory Leaves the Navigation Empty at First

When you start your Writory site, the navigation menu at the top of the site will be empty. The idea is to give you as much freedom as possible to design your navigation according to *your* requirements. You should only have links in the navigation if you really want them there. And in the proper order, too!

## Add Entries to Your Navigation Menu

The simplest way to create menu entries, is to to define them via front matter of your content files.

### Books

For example, if you want an entry to the list of your books, simply create an ``_index.md`` file in the folder ``content/books``. Within the file's front matter, set ``head`` as the menu and define the position of the page in the navigation.

```
title: Books
menu:
  head:
    weight: 1
```

Don't forget to add a title to this content page, otherwise Writory won't be able to show any on that page. By the way, you can add content and a summary to that page, too!

This is how the ``_index.md`` file looks for [writory.org/books](/books/):

```
---
title: Books
summary: Our small library of Writory books
menu:
  head:
    weight: 1
---

Find out with these fine books how to kick-start your book site with the [Writory theme](https://github.com/MichaelSchmidle/writory-hugo-theme/) and [Hugo](https://gohugo.io/), how to customize the theme to your needs—and why the heck anyone would need this:
```

### Series and Authors

The two taxonomies used by Writory can be added them the same way: Add the ``head`` menu to the front matter of the taxonomies' ``_index.md`` files.

Here's the source of the ``content/series/_index.md`` file for [writory.org/series](/series/):

```
---
title: Series
summary: Showcasing the series feature
menu:
  head:
    weight: 2
---

Just to show you how this feature works, we've created a little series of books called "Writory."
```

## Non-Content Page Entries

Hugo also allows to add further entries without using content files. See [Hugo's documentation](https://gohugo.io/content-management/menus/#add-non-content-entries-to-a-menu) for more details on how to configure menus via your site's configuration file.
