---
layout: docs
title: Tovuti Theme
description: Quick debrief of what has happened with the theme.
group: extend
aliases:
  - "/docs/5.2/extend/"
---


## Summary

Inside of variables.scss disable shadows

{{< example >}}
$enable-shadows:              false !default;
$font-family-sans-serif:      'Inter', system-ui, -apple-system, "Segoe UI", "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji" !default;
$font-family-monospace:       'JetBrains Mono', Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace !default;
$headings-font-family:        'Inter Tight', sans-serif !default;
$badge-font-family:                 $font-family-base !default;
$badge-font-weight:                 $font-weight-medium !default;
{{< /example >}}
