---
order: 4
title: Multi-Language Support
summary: How to add further languages to your Writory site
date: 2020-02-28
resources:
- name: cover
  src: ""
---

## Default Languages in Writory

Writory currently supports two languages out of the box:

* English [en]
* German [de]

## Switching the Default Language

Hugo defaults to English as primary language. Just set the ``defaultLanguage`` to ``de`` in your site's configuration file, if you want to switch from English to German as your only language.

Then create ``_index.de.md`` files in the three content directories ``books``, ``series``, and ``authors``. To each of these, add a ``title`` and corresponding ``url`` variable in the front matter.

Example for ``books/_index.de.md``:

```
---
title: Bücher
url: buecher
---
```

This way, Hugo picks up the proper titles and URLs for Writory's sections and taxonomies.

{{<alert class="wy-alert-warning my-5">}}
##### Warning

You might be tempted to define localized taxonomies in your site configuration (for example, using the German ``autor: autoren`` instead of the English ``author: authors``). **Be careful with that.**

Writory uses the English section ``books`` as well as the English taxonomies ``authors`` and ``series`` to build the navigation and localize the navigation via front matter in your content files.
{{</alert>}}

## Using Multiple Languages in Parallel

For parallel use of languages, there are a few more additional steps to take:

* Configure the languages to use as per [Hugo's documentation](https://gohugo.io/content-management/multilingual/).
* Translate settings from your site's configuration, like ``copyright``, ``params.description``, and ``thirdPartyReferences`` in the respective language sections.
* As explained above, add the ``_index.??.md`` files (including the appropriate language code in the file name) in the content folders ``books``, ``series``, and ``authors``.

## Adding Non-Default Languages to Writory

To add further languages beyond those provided per default, you have to provide the translations yourself. To achieve this, add the necessary translation files to the ``i18n`` folder of your site as per [Hugo's documentation](https://gohugo.io/content-management/multilingual/#translation-of-strings). As a template, you can use [Writory's original ``en.yml`` file](https://github.com/MichaelSchmidle/writory-hugo-theme/tree/master/i18n).

{{<alert class="wy-alert-primary mt-5">}}
##### Please Contribute!
Of course, I would be happy to add further default languages to Writory---so please, don't hesitate to submit your translation files to the [Writory repository on GitHub](https://github.com/MichaelSchmidle/writory-hugo-theme/)!
{{</alert>}}
