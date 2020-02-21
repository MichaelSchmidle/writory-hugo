---
order: 2
title: Color Schemes
summary: For everyone the right colors
date: 2020-01-31
resources:
- name: cover
  src: ""
---

## Available Color Schemes

Writory provides four color themes whose primary colors are picked from the [Mirage illustrations](https://icons8.com/ouch/style/mirage-1):

| Parameter Value               | Primary Color | RGB Hex | Example                  |
| ------------------------------|---------------|---------|--------------------------|
| ``medium-blue.css`` (default) | Medium Blue   | #0060b1 | {{<color hex="0060b1">}} |
| ``blue.css``                  | Blue          | #0200a5 | {{<color hex="0200a5">}} |
| ``violet.css``                | Violet        | #9600ac | {{<color hex="9600ac">}} |
| ``pinkish-red.css``           | Pinkish Red   | #e30040 | {{<color hex="e30040">}} |

Writory comes **by default with the medium-blue scheme**. In case you want to change the scheme, follow the instructions below.

## Configure Color Scheme

Inside your Hugo site configuration file, add the ``writory`` section to your ``params`` section. Inside the ``writory`` section, define the parameter ``colorScheme``.

If you use a ``config.yml`` file and wanted to use the scheme of pinkish red, it would look like this:

```
params:
  writory:
    colorScheme: pinkish-red.css
```
