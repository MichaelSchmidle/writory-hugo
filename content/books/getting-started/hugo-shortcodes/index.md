---
order: 3
title: Hugo Shortcodes
summary: Making it easy to use common GUI elements in your books
date: 2020-01-29
resources:
- name: cover
  src: ""
- src: orange-tabby-cat-on-white-table-3687957.jpg
  title: "Orange Tabby Cat on White Table (Image: [Matthias Oben](https://www.pexels.com/photo/orange-tabby-cat-on-white-table-3687957/))"
---

## Figure

Example:

{{<figure src="https://via.placeholder.com/720x480">}}
Image: [placeholder.com](https://placeholder.com)
{{</figure>}}

The corresponding Shortcode in Markdown:

```
{{<htmlUnescape>}}{{&lt;figure src=&quot;https://via.placeholder.com/720x480&quot;&gt;}}
Image: [placeholder.com](https://placeholder.com)
{{&lt;/figure&gt;}}{{</htmlUnescape>}}
```

It requires the attribute ``src``. This can either be the reference to a [Page Resource](https://gohugo.io/content-management/page-resources/), to an image in your ``static`` folder or to any other image with an URL.

It accepts one optional attribute, ``class``. Use this attribute to override the Writory style with combinations of [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/). **Please note:** The class targets the ``<img>`` tag inside the ``<figure>`` tag.

If the ``src`` attribute points to a Page Resource, its title will be used as caption of the figure. (This can be overridden by providing a specific caption between the opening ``{{<htmlUnescape>}}{{&lt;figure&gt;}}{{</htmlUnescape>}}`` and closing ``{{<htmlUnescape>}}{{&lt;/figure&gt;}}{{</htmlUnescape>}}`` tags.) See the following example:

{{<figure src="orange-tabby-cat-on-white-table-3687957.jpg" />}}

The corresponding Shortcode in Markdown:

```
{{<htmlUnescape>}}{{&lt;figure src=&quot;orange-tabby-cat-on-white-table-3687957.jpg&quot;&gt;}}{{</htmlUnescape>}}
```

## Alert

Examples:

{{<alert class="wy-alert-primary">}}This is a primary alert.{{</alert>}}
{{<alert class="wy-alert-secondary">}}This is a secondary alert.{{</alert>}}
{{<alert class="wy-alert-success">}}This is a success alert.{{</alert>}}
{{<alert class="wy-alert-danger">}}This is a danger alert.{{</alert>}}
{{<alert class="wy-alert-warning">}}This is a warning alert.{{</alert>}}
{{<alert class="wy-alert-info">}}This is an info alert.{{</alert>}}
{{<alert class="wy-alert-light">}}This is a light alert.{{</alert>}}
{{<alert class="wy-alert-dark mb-5">}}This is a dark alert.{{</alert>}}

The corresponding Shortcodes in Markdown:

```
{{<htmlUnescape>}}{{&lt;alert class=&quot;wy-alert-primary&quot;&gt;}}This is a primary alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-secondary&quot;&gt;}}This is a secondary alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-success&quot;&gt;}}This is a success alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-danger&quot;&gt;}}This is a danger alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-warning&quot;&gt;}}This is a warning alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-info&quot;&gt;}}This is an info alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-light&quot;&gt;}}This is a light alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;wy-alert-dark&quot;&gt;}}This is a dark alert.{{&lt;/alert&gt;}}{{</htmlUnescape>}}
```

It accepts one optional attribute, ``class``. Use this attribute to style the alert with the above Writory classes—or with combinations of [Bootstrap Alerts classes](https://getbootstrap.com/docs/4.4/components/alerts/) and/or [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).

## Cite

Example:

> This is a famous blockquote
{{<cite adapted="true">}}This is the cite{{</cite>}}

The corresponding Shortcode in Markdown:

```
{{<htmlUnescape>}}&gt; This is a famous blockquote
{{&lt;cite adapted=&quot;true&quot;&gt;}}This is the cite{{&lt;/cite&gt;}}{{</htmlUnescape>}}
```

It accepts one optional attribute, ``adapted``. Set this attribute to ``true`` to signal that you have adapted the original quote.

## Card

Example:

{{<card class="shadow mb-5" markdownify="true">}}
### Example Card
This is a small example of a card.
{{</card>}}

The corresponding Shortcode in Markdown:

```
{{<htmlUnescape>}}{{&lt;card class=&quot;shadow&quot; markdownify=&quot;true&quot;&gt;}}
### Example Card
This is a small example of a card.
{{&lt;/card&gt;}}{{</htmlUnescape>}}
```

It accepts two optional attributes, ``class`` and ``markdownify``.

Use the ``class`` attribute to style the card with combinations of [Bootstrap Card classes](https://getbootstrap.com/docs/4.4/components/card/) and/or [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).

Define with the boolean ``markdownify`` attribute whether the card's content should be interpreted as Markdown. If false or omitted, the content is rendered as-is.

## Link Button

Examples:

{{<link-button href="/books/" class="btn-primary">}}List books{{</link-button>}}
{{<link-button href="/books/" class="btn-secondary">}}List books{{</link-button>}}
{{<link-button href="/books/" class="btn-outline-info">}}List books{{</link-button>}}

The corresponding Shortcodes in Markdown:

```
{{<htmlUnescape>}}{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-primary&quot;&gt;}}List books{{&lt;/link-button&gt;}}
{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-secondary&quot;&gt;}}List books{{&lt;/link-button&gt;}}
{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-outline-info&quot;&gt;}}List books{{&lt;/link-button&gt;}}{{</htmlUnescape>}}
```

It accepts two optional attributes, ``href`` and ``class``.

Define the ``href`` attribute to provide a link target address, just like you would in regular HTML anchor tags à la ``<a href="https://writory.org/">Writory</a>``.

Use the ``class`` attribute to style the link button with combinations of [Bootstrap Buttons classes](https://getbootstrap.com/docs/4.4/components/buttons/) and/or [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).
