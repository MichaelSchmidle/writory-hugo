---
order: 4
title: "Navigation"
summary: "Learn How to Customize Your Navigation Menu"
date: 2020-02-26
---

## Default Navigation

Writory defaults to the following navigation---just like on this site:

* Books, leading to the URL ``/books/``
* Series, leading to the URL: ``/series/``
* Authors, leading to the URL: ``/authors/``

## Customize Your Navigation Menu

In case you want to customize your navigation menu, you can do so by defining a ``header`` menu. As per [Hugo's documentation](https://gohugo.io/content-management/menus/). there are two ways to do this:

* By adding content files via their front matter to the ``header`` menu
* By defining the ``header`` menu in your site's configuration file

In any case, please remember that by defining a ``header`` menu, you'll effectively override the *entire* default navigation of Writory. In other words: Whether you want to completely replace the navigation or just add a fourth menu entry, you'll have to define *all* entries yourself.

The default ``header`` menu can be recreated like this in your site's ``yml`` configuration file:

```
menu:
  head:
    - identifier: books
      name: Books
      url: /books/
      weight: 1
    - identifier: series
      name: Series
      url: /series/
      weight: 2
    - identifier: authors
      name: Authors
      url: /authors/
      weight: 3
```

{{<alert class="wy-alert-warning mt-5">}}
##### Warning

The "Series" and "Authors" navigation entries represent the site's taxonomies. If you customize the taxonomy settings, remember to customize your navigation accordingly---and vice versa!
{{</alert>}}
