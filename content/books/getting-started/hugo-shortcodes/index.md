---
order: 3
title: Hugo Shortcodes
summary: Making it easy to use common GUI elements in your books
date: 2020-01-29
resources:
- name: cover
  src: ""
---

## Alert

Examples:
{{<card class="mb-5">}}
{{<alert class="sy-alert-primary">}}This is a primary alert.{{</alert>}}
{{<alert class="sy-alert-secondary">}}This is a secondary alert.{{</alert>}}
{{<alert class="sy-alert-success">}}This is a success alert.{{</alert>}}
{{<alert class="sy-alert-danger">}}This is a danger alert.{{</alert>}}
{{<alert class="sy-alert-warning">}}This is a warning alert.{{</alert>}}
{{<alert class="sy-alert-info">}}This is an info alert.{{</alert>}}
{{<alert class="sy-alert-light">}}This is a light alert.{{</alert>}}
{{<alert class="sy-alert-dark mb-5">}}This is a dark alert.{{</alert>}}
{{</card>}}

The corresponding Shortcodes in Markdown:
```
{{<htmlUnescape>}}{{&lt;alert class=&quot;sy-alert-primary&quot;&gt;}}This is a primary alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-secondary&quot;&gt;}}This is a secondary alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-success&quot;&gt;}}This is a success alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-danger&quot;&gt;}}This is a danger alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-warning&quot;&gt;}}This is a warning alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-info&quot;&gt;}}This is an info alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-light&quot;&gt;}}This is a light alert.{{&lt;/alert&gt;}}
{{&lt;alert class=&quot;sy-alert-dark&quot;&gt;}}This is a dark alert.{{&lt;/alert&gt;}}{{</htmlUnescape>}}
```

It accepts one optional attribute, ``class``. Use this attribute to style the alert with the above Writory classes—or with combinations of [Bootstrap Alerts classes](https://getbootstrap.com/docs/4.4/components/alerts/) and/or [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).

## Blockquote

Example:
{{<card class="mb-5">}}
{{<blockquote class="">}}This is a blockquote.{{</blockquote>}}
{{</card>}}

The corresponding Shortcode in Markdown:
```
{{<htmlUnescape>}}{{&lt;blockquote class=&quot;&quot;&gt;}}This is a blockquote.{{&lt;/blockquote&gt;}}{{</htmlUnescape>}}
```

It accepts one optional attribute, ``class``. Use this attribute to override the Writory style of the blockquote with combinations of [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).

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

{{<card class="mb-5">}}
{{<link-button href="/books/" class="btn-primary">}}List books{{</link-button>}}
{{<link-button href="/books/" class="btn-secondary">}}List books{{</link-button>}}
{{<link-button href="/books/" class="btn-outline-info">}}List books{{</link-button>}}
{{</card>}}

The corresponding Shortcodes in Markdown:
```
{{<htmlUnescape>}}{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-primary&quot;&gt;}}List books{{&lt;/link-button&gt;}}
{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-secondary&quot;&gt;}}List books{{&lt;/link-button&gt;}}
{{&lt;link-button href=&quot;/books/&quot; class=&quot;btn-outline-info&quot;&gt;}}List books{{&lt;/link-button&gt;}}{{</htmlUnescape>}}
```

It accepts two optional attributes, ``href`` and ``class``.

Define the ``href`` attribute to provide a link target address, just like you would in regular HTML anchor tags à la ``<a href="https://writory.org/">Writory</a>``.

Use the ``class`` attribute to style the link button with combinations of [Bootstrap Buttons classes](https://getbootstrap.com/docs/4.4/components/buttons/) and/or [Bootstrap Utilities classes](https://getbootstrap.com/docs/4.4/utilities/borders/).
