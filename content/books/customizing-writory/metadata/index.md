---
order: 3
title: Metadata
summary: Add metadata like copyright and licenses to your site
date: 2020-01-31
resources:
- name: cover
  src: ""
---

## Available Metadata Configurations

If configured in your site configuration file, Writory currently respects the following customizations. Future releases of Writory may support more metadata configurations.

### Copyright Notice

Writory by default shows the generic copyright notice ``Copyright © {{ .Site.LastChange }} · All rights reserved`` in the footer. Please note that this date variable only is populated by Hugo if at least one [chapter](/books/getting-started/building-blocks/#chapters) carries a ``date`` in its front matter.

The notice can be customized by two parameters:
* ``copyright``: Licensing information as string (may contain Markdown)
* ``authors``: Copyright holders as list of elements in the ``params`` section (elements may contain Markdown)

These parameters are defined as per the following example ``config.yml`` file of this site:

```
copyright: "Original content released under the [MIT License](https://github.com/MichaelSchmidle/writory-hugo/blob/master/LICENSE)"

params:
  authors: ["[Michael Schmidle](https://blog.ypertex.com/authors/michael-schmidle/)"]
```

### Open Graph Image

When you post links to your Writory site or pages to social platforms, they'll grab some metadata from these links. This allows them to display previews of the linked pages to their users.

For books as well as series, the ``cover`` resource as configured in the respective front matter will be referenced as preview image—the Open Graph image. For all other pages, you can conigure a default cover in your site configuration's ``params``.

For example, you can use your [logo or logogram](/books/customizing-writory/logo-and-logogram/) for these previews:

```
params:
  cover: writory-logogram.png
```

## Third Party References

Writory per default includes a few references in the footer: to [Hugo](https://gohugo.io/), to itself, and to [Icons8](https://icons8.com/).

If necessary, these third party references can be customized via the configuration parameter ``thirdPartyReferences`` in the ``params`` section. The parameter may contain Markdown.

{{<alert class="wy-alert-warning my-5">}}
##### Warning

Remember to **remove the illustrations** from your site if you decide to omit the reference to Icons8. They only may be used with the attribution.
{{</alert>}}

Example of the ``config.yml`` file of this site:

```
params:
    thirdPartyReferences: ["Mirage illustrations licensed by [Icons8 LLC.](https://icons8.com/)", "Made with [Hugo](https://gohugo.io/) and [Bootstrap](https://getbootstrap.com/)"]
```
