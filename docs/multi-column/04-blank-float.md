---
title: Blank Callout and Float (Aside)
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

example
`> [!warning|right-small]`
