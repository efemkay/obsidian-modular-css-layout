---
title: Using Callout
parent: Multi Column
nav_order: 2
---

# MC Using Callout
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Overview
- Custom Callout available
	- `> [!multi-column]`
	- `> [!blank-container]`

This layout take advantage of the new Obsidian Callout feature. Using the callout as parent 'div' to house the sub callout. You can nest as many sub-callouts/dataview codeblocks within the [!multi-column] callout - it will create a sub-callout/dataview renders with minimum width of 200px (can be change using Sytle Settings plugin). The sub-callout/dataview renders will expand if [!multi-column] has extra space or overflow to next row if it doesn't.

Once you enabled the css snippet, you use this feature by creating a custom callout like example below

```
> [!multi-column]
>
>> [!note]+ Work
>> your notes or lists here. using markdown formatting
>
>> [!warning]+ Personal
>> your notes or lists here. using markdown formatting
>
>> [!summary]+ Charity
>> your notes or lists here. using markdown formatting
```

> note that when you insert callout within callout, the line separating the callouts should only use single angle bracket (">")

## Width Control
You can control sub-callout (within Multi-Column callout) on per callout and per note basis by specifying the callout-metadata element. So far, there's only a discrete options per below
- `min-0` - to override and disable min width set in Style Settings
- `wide-2` - give callout twice the size
- `wide-3` - three times the size
- `wide-4` - four times the size
- `wide-5` - five times the size

> #### When Pairing with sub-callout with min width
> By default, sub-callout within multi-column callout has min width of 200px (unless you changed it via Style Settings). Applying `wide-x` metadata for sub-callout that paired with those callout will have different sizing behaviour

> #### Understanding callout type and callout metadata
> - `> [!<callout-type>]` e.g. `> [!Summary]`
> - `> [!<callout-type>|<callout-metadata>]` e.g. `> [!Summary|wide-2]`

## No Wrap Control
Additional feature to create a "fixed" multi column callout despite of the note or window size. Instead of wrapping and flowing to next line, this will instead have horizontal scrollbar.

To create no wrap multi column, use the following syntax i.e. `[!multi-column|no-wrap]`

> #### Limitation on No-Wrap Multi Column
> Width Control (different width for sub-callout) for now is not valid for No-Wrap Multi Column. Columns will be mostly follow the minimum width -- it has separate minimum width than the Wrapped Multi Column

## Examples

#### Example Screenshot - Multi Column (general)
<img src="https://user-images.githubusercontent.com/42369515/163700561-c8d62aa3-0ac8-488c-a80e-8bfb3b539ca8.png" height="350px" />

#### Example Screenshot - Multi Column Callout Width Control
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-width-control.png" height="350px" />

#### Example GIF
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/how%20to%20install%20and%20enable%20MCL.gif" height="350px" />
