---
title: Blank Callout and Float
parent: Multi Column
nav_order: 4
---

# Blank and Float Callout
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Blank Callout
- Using custom callout `[!blank-container]` or `[!blank]`
    - Use it as an invisible container/div to encapsulate other contents like paragraph or list items. Use in combination of `[!multi-column]` callout to place multiple paragraphs/content side by side without the callout background/color artefacts
    - Also useful to render things in Live Preview which normally need Reading View like List Columns/Grid/Card

## Side Column / Floating Column
- Using Callout metadata
	- `> [!<anycallout>|<left|right>-<small|medium|large>]`
	- `> [!blank-container|<left|right}-<small|medium|large>]`
- To have the effect applicable also in Live Preview use the following callout metadata instead (prepend `float-` before `right` or `left`)
    - `> [!<anycallout>|float-<left|right>-<small|medium|large>]`
    - `> [!blank-container|float-<left|right}-<small|medium|large>]`
> Note that editing float in Live Preview will be a bit off (or "janky"). Navigate using keyboard instead of mouse/trackpad and even better use Source Mode

example
`> [!warning|right-small]`
