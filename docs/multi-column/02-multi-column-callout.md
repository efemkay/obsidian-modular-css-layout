---
title: Multi Column Callout
parent: Multi Column
nav_order: 2
---

# Multi Column Callout
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Overview
Multi Column Callout layout take advantage of Obsidian Callout - leveraging it as parent 'div' to house the sub callout (including Dataview results block). You can nest as many sub-callouts within it

The sub-callout will expand if `[!multi-column]` callout has extra space or overflow to next row if it doesn't. Some degree of control is available - see Additional Controls below

![](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/hero-mc-callout.png)

### How to Use / Basic Syntax
Here's a quick steps to create the Multi Column Callout. It's best to start with sub-callouts first to avoid getting confused on how to nest them.
1. Create the sub-callouts you want to include. In the example below they are `[!note]`, `[!warning]` and `[!summary]`
2. Wrap / encapsulate those sub-callouts with `[!multi-column]` callout

Here's an example markdown
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

> Note that when you insert callout within callout, the line separating the callouts should only use single angle bracket (">")


{: .note-title }
> What Counts as Column in a `[!multi-column]`?
>
> By default, another callout (aka sub-callout) within `[!multi-column]` is how you create a "column". But this snippets do provide a few alternatives
> - immediate dataview block (either table or list)
> - immediate blockquote
> - ordered/unordered list (but need to have `<br/>` tag between lists due to how obsidian override "markdown loose list")


## Additional Controls
### Fixed Width Option for `[!multi-column]`
This option will allow you to create fixed width multi column callout that doesn't expand. You can specify it to either align to the center, left or right. This may be useful if you want to create dashboard with icon that you want to stay clustered together rather than spread to fill in the space.

To create a fixed-width multi column, use the following syntax:
- `[!multi-column|center-fixed]` - for align to the center
- `[!multi-column|left-fixed]` - for align to the left
- `[!multi-column|right-fixed]` - for align to the right

Here's an example markdown
```
> [!multi-column|center-fixed]
>
>> [!blank-container]
>> ![[icon 1.jpg]]
>
>> [!blank-container]
>> ![[icon 2.jpg]]
>
>> [!blank-container]
>> ![[icon 3.jpg]]
```

### No Wrap Option for `[!multi-column]`
This option will allow you to create single row multi column callout. Horizontal scrollbar will appear when the sub-callouts exceed the width of the `[!multi-column]`. To create no wrap multi column, use the following syntax i.e. `[!multi-column|no-wrap]`.

Here's an example markdown
```
> [!multi-column|no-wrap]
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

{: .note-title }
> Limitation on No-Wrap Multi Column
>
> Width Control (different width for sub-callout) for now is not valid for No-Wrap Multi Column. Columns will be mostly follow the minimum width -- it has separate minimum width than the Wrapped Multi Column

### Width Control
You can control sub-callout width by specifying the custom width option in the callout-metadata element (do NOT apply to `[!multi-column]` callout itself. So far, there's only a discrete options per below:
- `min-0` - to override and disable min width set in Style Settings
- `wide-2` - give callout twice the size
- `wide-3` - three times the size
- `wide-4` - four times the size
- `wide-5` - five times the size

Here's an example markdown
```
> [!multi-column]
>
>> [!note|wide-3]+ Work
>> your notes or lists here. using markdown formatting
>
>> [!warning|wide-2]+ Personal
>> your notes or lists here. using markdown formatting
>
>> [!summary|min-0]+ Charity
>> your notes or lists here. using markdown formatting
```

{: .note-title }
> When Pairing with sub-callout with min width
>
> By default, sub-callout within multi-column callout has min width of 200px (unless you changed it via Style Settings). Applying `wide-x` metadata for sub-callout that paired with those callout will have different sizing behaviour

{: .note-title }
> Understanding callout type and callout metadata
>
> - `> [!<callout-type>]` e.g. `> [!Summary]`
> - `> [!<callout-type>|<callout-metadata>]` e.g. `> [!Summary|wide-2]`

### Additional Global Settings via Style Settings
If you have Style Settings plugin installed, you may control the following aspects (go to `Style Settings > Modular CSS Layout - Multi Column > Multi Column Callout`)
- Hide / Show SNW Indicator for images in Float Callout
- Adjust minimum width for general sub-callout and No-Wrap sub-callout
- Adjust gap between sub-callout and margin between sub-callout

## Examples

#### Standard Multi-Column Callout
> ![](/docs/assets/mc-callout-standard.png)
> ```
> > [!multi-column]
> >
> >> [!note]+ Use Case
> >> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
> >> ##### User Case Background
> >> Vitae nunc sed velit dignissim sodales. In cursus turpis massa tincidunt dui ut ornare lectus.
> >
> >> [!warning]+ Resources
> >> #### Requirement
> >> - Lorem ipsum dolor sit amet
> >> - Vitae nunc sed velit dignissim sodales.
> >> - In cursus turpis massa tincidunt dui ut ornare lectus.
> >
> >> [!todo]+
> >> - [x] Define Use Case
> >> - [ ] Craft User Story
> >> - [ ] Develop draft sketches
> ```

---

#### Icon Links Dashboard using Fixed Width option
> ![example of list column](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-fixed-width.png)
>
> ```markdown
> ## Icon Links Dashboard using `[!multi-column|center-fixed-small]`
>
> > [!multi-column|center-fixed-small]
> >
> >> [!blank|center]
> >> [![lightbulb icon|80](https://img.icons8.com/ios/250/FFFFFF/light-on.png) <br/> Interests](target%20note.md)
> >>
> >> [![macbook icon|80](https://img.icons8.com/ios/250/FFFFFF/macbook.png) <br/> Technology](target%20note.md)
> >
> >> [!blank|center]
> >> [![brain icon|80](https://img.icons8.com/ios/250/FFFFFF/brain.png) <br/> Life & Wisdom](target%20note.md)
> >>
> >> [![briefcase icon|80](https://img.icons8.com/ios/250/FFFFFF/business.png) <br/> Work](target%20note.md)
> >
> >> [!blank|center]
> >> [![running icon|80](https://img.icons8.com/ios/250/FFFFFF/sports-mode.png) <br/> Health](target%20note.md)
> >>
> >> [![home icon|80](https://img.icons8.com/ios/250/FFFFFF/house-with-a-garden.png) <br/> Family](target%20note.md)
>
> ```

---

#### Example Screenshot - Multi Column Callout with Width Control
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-width-control.png" height="350px" />

---

#### Example GIF - Install the snippet and apply Multi Column Callout
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/how%20to%20install%20and%20enable%20MCL.gif" height="350px" />
