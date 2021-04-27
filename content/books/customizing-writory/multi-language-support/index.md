---
order: 5
title: Multi-Language Support
summary: How to add further languages to your Writory site
date: 2020-02-28
resources:
- name: cover
  src: ""
---

## Default Languages in Writory

Writory currently supports two languages out of the box: English and German.

The navigation is [localized](https://github.com/MichaelSchmidle/writory-hugo-theme/tree/master/i18n) according to the following table:

| Language, code  | Name, URL of books section | Name, URL of series taxonomy | Name, URL of authors taxonomy |
|-----------------|----------------------------|------------------------------|-------------------------------|
| English, ``en`` | Books, ``books``           | Series, ``series``           | Authors, ``authors``          |
| German, ``de``  | Bücher, ``buecher``        | Serien, ``serien``           | Autoren, ``autoren``          |

## Switching the Default Language

Hugo defaults to English as primary language. If you want to switch from English to another language as your only language, follow these steps:

1. Change your site's ``defaultContentLanguage``
2. Update your site's taxonomies

The first step is done easily by adding one line to your configuration file. Here's an example of a ``config.yml`` file setting German as default content language:

```
defaultContentLanguage: de
```

The second party involves slightly more changes. Begin by translating the English taxonomies ``series: series`` and ``author: authors`` according to the translation table above. For German, a ``config.yml`` file would look like this:

```
taxonomies:
    serie: serien
    autor: autoren
```

Then create your content in the proper subfolders of your content folder. For example, to publish books in German, put your content into the subfolders ``buecher``, ``serien`` and ``autoren``. Remember to use these directories when creating new content via archetypes:

```
hugo new --kind book buecher/mein-erstes-buch
hugo new --kind chapter buecher/mein-erstes-buch/mein-erstes-kapitel
hugo new --kind series serien/meine-erste-serie
hugo new --kind author autoren/mein-erster-autor
```

{{<alert class="wy-alert-warning mt-5">}}
##### Caution

Make sure that Hugo can properly map your content. This requires an ``_index.md`` file in each localized folder that defines the appropriate ``type`` in the front matter. If you want to use German content, for example:

* ``/content/buecher/_index.md`` defines ``type: books`` and ``title: Bücher``
* ``/content/serien/_index.md`` defines ``type: series`` and ``title: Serien``
* ``/content/autoren/_index.md`` defines ``type: authors`` and ``title: Autoren``

(You can put the ``type`` declaration inside a ``cascade`` block to [automatically apply the type](https://gohugo.io/content-management/front-matter/#front-matter-cascade) to all the content inside the respective directory.)
{{</alert>}}

## Using Multiple Languages in Parallel

For parallel use of languages, there are a few more additional steps to take:

1. Configure the languages to use as per [Hugo's documentation](https://gohugo.io/content-management/multilingual/).
2. Translate settings from your site's configuration, like ``copyright``, ``params.description``, and ``thirdPartyReferences`` in the respective language sections.
3. As explained above, add the localized content in their respective content folders. Make sure that folder names, taxonomy names and translations match.
4. Add the language code to all non-default language files. Example: If English is not your default language, name your content files ``_index.en.md`` or ``index.en.md``.

## Adding Non-Default Languages to Writory

To add further languages beyond those provided per default, you have to provide the translations yourself. To achieve this, add the necessary translation files to the ``i18n`` folder of your site as per [Hugo's documentation](https://gohugo.io/content-management/multilingual/#translation-of-strings). As a template, you can use [Writory's original ``en.yml`` file](https://github.com/MichaelSchmidle/writory-hugo-theme/tree/master/i18n).

{{<alert class="wy-alert-primary mt-5">}}
##### Please Contribute

Of course, I would be happy to add further default languages to Writory---so please, don't hesitate to submit your translation files to the [Writory repository on GitHub](https://github.com/MichaelSchmidle/writory-hugo-theme/)!
{{</alert>}}
