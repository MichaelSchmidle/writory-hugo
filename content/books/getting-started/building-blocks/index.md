---
order: 2
title: Building Blocks
summary: Understanding the blocks available to build your book site
date: 2020-01-28
resources:
- name: cover
  src: ""
- src: author-links.png
  title: Links to an author's profiles on external platforms with corresponding icons
---

## Books

Books are what Hugo calls ["Content Sections"](https://gohugo.io/content-management/sections/) or ["Branch Bundles."](https://gohugo.io/content-management/page-bundles/) They basically are collections of chapters that together make up a story.

They are stored in ``_index.md`` files within the book's directory ``books/example-book``. Note the leading underscore in the file name.

Books are defined by the following [front matter](https://gohugo.io/content-management/front-matter/):

* ``layout``: **Don't change or remove this metadata.** It tells Hugo to render a book like a TOC—otherwise, it'd get rendered as a chapter. (By the way, "TOC" means "Table of Contents.")
* ``title``: String defining the title of the book.
* ``summary``: Optional string summarizing the content of the book. May contain Markdown.
* ``authors``: Optional array of authors. The names should match the authors' ``urlize``d file names. See [Authors](#authors) below.
* ``series``: Optional string referencing the series of books this book belongs to. Like the movie "The Force Awakens" belongs to the "Star Wars" series. The name should match the series' ``urlize``d file names. See [Series](#series) below.
* ``resources``: Optional [Page Resources](https://gohugo.io/content-management/page-resources/) for the book cover.
* ``featured``: Optional integer defining the position in the book list. The lower the number, the higher in the list.
* ``ended``: Boolean, defining whether the story in the book has ended or more chapters will follow in the future.
* ``draft``: Boolean, whether the book is considered in draft status.

Create a new book with the following command:

```
hugo new --kind book books/title-of-your-new-book
```

## Chapters

Chapters are ["Leaf Bundles"](https://gohugo.io/content-management/page-bundles/) or "Regular Pages" in Hugo jargon. They contain the original content of their books.

Chapters are stored as ``index.md`` files within the chapter's directory ``books/example-book/example-chapter`` (which is a subdirectory of the book they belong to). 

They are defined by the following front matter:

* ``order``: Integer defining the position in the chapter list. The lower the number, the higher in the list. Is used to display "Chapter 2 of 9."
* ``title``: String defining the title of the chapter
* ``summary``: Optional string summarizing the content of the chapter. May contain Markdown.
* ``date``: Date, required to display the proper copyright year in the footer of the site.
* ``resources``: Optional [Page Resources](https://gohugo.io/content-management/page-resources/). Not yet in use by the theme.
* ``draft``: Boolean, whether the chapter is considered in draft status.

Create a new chapter with the following command:

```
hugo new --kind chapter books/existing-book/title-of-your-new-chapter
```

## Series

Series are used to bundle related books, called a ["Taxonomy"](https://gohugo.io/content-management/taxonomies/) in Hugo terms. While a series can contain many books, a single book can only belong to one series. Imagine the movie "Infinity Wars" which is part of—and only part of—the Avengers movie series.

They are stored in ``_index.md`` files within the series' subdirectory ``series/example-series``. Note the leading underscore in the file name. The name of the subdirectory needs to match the book's references and vice versa. The series reference "Example Series" matches the folder name ``example-series``.

Series are defined by the following front matter:

* ``title``: String defining the title of the series
* ``summary``: Optional string summarizing the series of books. May contain Markdown.
* ``resources``: Optional [Page Resources](https://gohugo.io/content-management/page-resources/) for the series' cover.
* ``featured``: Optional integer defining the position in the series list. The lower the number, the higher in the list.
* ``draft``: Boolean, whether the series is considered in draft status.

Create a new series with the following command:

```
hugo new --kind series series/title-of-your-new-series
```

## Authors

As series, authors are another taxonomy. Books can be written by many authors and authors can have written many books.

Information about authors are stored in ``_index.md`` files within each author's directory ``authors/example-author``. Note the leading underscore in the file name. The name of the subdirectory needs to match the book's references and vice versa. The author reference "Example Author" matches the folder name ``example-author``.

* ``title``: String defining the name of the author
* ``summary``: Optional string summarizing the biography of the author. May contain Markdown.
* ``links``: Optional array of links, see [below for more information](#authors-links).
* ``resources``: Optional [Page Resources](https://gohugo.io/content-management/page-resources/) for the author's cover (not in use so far) and their avatar.
* ``featured``: Optional integer defining the position in the author list. The lower the number, the higher in the list.
* ``draft``: Boolean, whether the author page is considered in draft status.

Create a new author page with the following command:

```
hugo new --kind author authors/name-of-the-new-author
```

### Authors' Links

The ``links`` array lets authors provide links to their online identity: to their website or blog, to their social media profiles, and so on. Since every individual is present on different platforms, Writory lets authors set their own links.

This is how it works: Every item in the ``links`` array consists of 2-3 pieces of information:

* Required: the name of the platform
* Required: the address of the platform
* Optional: the icon class for the platform

The format is: ``Platform: [https://example.com/, icon class]``. If you wanted to add links to your author profile for your blog as well as LinkedIn, Twitter, and GitHub profiles, add the following lines to the front matter of your author's ``_index.md`` file:

```
links: [
  Blog: [https://blog.example.com/, las la-link],
  LinkedIn: [https://www.linkedin.com/in/example/, lab la-linkedin-in],
  Twitter: [https://twitter.com/example/, lab la-twitter],
  GitHub: [https://github.com/example/, lab la-github]
]
```

The icon class is taken from the free [Line Aweseome](https://icons8.com/line-awesome) icon set. If you omit the icon class, no icon will be shown for the link.

The above lines result in the following screenshot:

{{<figure src="author-links.png" />}}

{{<alert class="wy-alert-info">}}
##### Info

If you want that all authors on your Writory site use the same template: Simply provide your own [archetype](https://gohugo.io/content-management/archetypes/) file for authors with a predefined set of platforms and corresponding icon classes.

Alternatively, you can also overwrite the ``author-links.html`` partial file. Just put a file with the same name in the ``partials`` folder of your site to handle links your way.
{{</alert>}}
