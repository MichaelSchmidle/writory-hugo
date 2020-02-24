---
order: 1
title: Logo and Logogram
summary: Brand your Writory site
date: 2020-02-02
resources:
- name: cover
  src: ""
---

## Difference Between Logo and Logogram

The iconic part of logos is called *logogram*, while any text is called *logotype*. Together, logogram and logotype constitute your *logo*.

If configured, Writory takes your logo and logogram and displays them in a few places—otherwise it'll use your site's title as configured in ``.Site.Title``:

* The **logo** is shown on the home page.
* The **logogram** is shown in the navigation bar and footer.

{{<figure src="/writory-logo-h.png">}}
Writory's logo
{{</figure>}}

{{<figure src="/writory-logogram.png" class="w-25">}}
Writory's logogram
{{</figure>}}

## Configure Logo

Define the parameter ``logo`` inside the ``params`` setion of your site's configuration file.

If you use a ``config.yml`` file, it would look like this:

```
params:
  logo: writory-logo.svg
```

Hugo will look for this logo file inside the ``static`` folder of your site. Once configured, your logo will be shown on the home page of your site (instead of the textual name of your site).

## Configure Logogram

Define the parameter ``logogram`` inside the ``params`` section of your site's configuration file.

If you use a ``config.yml`` file, it would like this:

```
prarams:
  logogram: writory-logogram.svg
```

Hugo will look for this logogram file inside the ``static`` folder of your site. Once configured, your logogram will be shown in the navigation bar of your site (instead of the textual name of your site).

## Use Custom Favicons

Writory comes with a default set of favicons. In case you want to use your own favicons to go along with your logo, just put your favicon files inside the ``static`` folder of your site to override the default ones.

Writory uses the following icons:

* favicon.ico
* apple-touch-icon-57x57.png
* apple-touch-icon-60x60.png
* apple-touch-icon-72x72.png
* apple-touch-icon-76x76.png
* apple-touch-icon-114x114.png
* apple-touch-icon-120x120.png
* apple-touch-icon-144x144.png
* apple-touch-icon-152x152.png
* apple-touch-icon-180x180.png
* favicon-16x16.png
* favicon-32x32.png
* favicon-96x96.png
* android-chrome-192x192.png
* smalltile.png
* mediumtile.png
* widetile.png
* largetile.png

If you don't want to use the entire or a completely different set, Writory lets you do that, too:

* Create a file called ``_favicons.html`` inside the ``layouts/partials`` folder of your site. In this file, provide the HTML referencing your icons.
* Put all icons referred to by your HTML into the ``static`` folder of your site.

Writory's default partial looks like this:

```
<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon" />
<link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57x57.png">
<link rel="apple-touch-icon" sizes="60x60" href="/apple-touch-icon-60x60.png">
<link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-72x72.png">
<link rel="apple-touch-icon" sizes="76x76" href="/apple-touch-icon-76x76.png">
<link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114x114.png">
<link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon-120x120.png">
<link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144x144.png">
<link rel="apple-touch-icon" sizes="152x152" href="/apple-touch-icon-152x152.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
<link rel="icon" type="image/png" href="/favicon-16x16.png" sizes="16x16">
<link rel="icon" type="image/png" href="/favicon-32x32.png" sizes="32x32">
<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96">
<link rel="icon" type="image/png" href="/android-chrome-192x192.png" sizes="192x192">
<meta name="msapplication-square70x70logo" content="/smalltile.png" />
<meta name="msapplication-square150x150logo" content="/mediumtile.png" />
<meta name="msapplication-wide310x150logo" content="/widetile.png" />
<meta name="msapplication-square310x310logo" content="/largetile.png" />
```

## Use Your Logo/-gram as Open Graph Image

See the metadata option [Open Graph Image](/books/customizing-writory/metadata/#open-graph-image).
