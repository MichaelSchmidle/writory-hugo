---
order: 4
title: Custom Navigation
summary: Define Your Own Navigation
date: 2020-03-03T08:59:00+01:00
resources:
- name: cover
  src: ""
---

## Default Header Navigation

Writory comes with the following default header navigation:

1. "Books", leading to ``/books/``
1. "Series", leading to ``/series/``
1. "Authors", leading to ``/authors/``

## Define Your Own Header Navigation

You are free to define your own header navigation. Follow [Hugo's documentation](https://gohugo.io/content-management/menus/) and build a menu called ``header`` in your site's configuration.

Example of a site's ``config.yml`` file for adding a custom entry at the second position:

```
menu:
    header:
        - name: Books
          url: /books/
          weight: 1
        - name: About Us
          url: /about/
          weight: 2
        - name: Series
          url: /series/
          weight: 3
        - name: Authors
          url: /authors/
          weight: 4
```
