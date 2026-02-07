---
title: List Grid
parent: Multi Column
nav_order: 6
---

# List Grid
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Overview
List Grid layout will allow you to create multi column and multi row layout using a combinatio of (a) unordered lists (i.e.  `- list item`) and (b) either hashtag or css class at frontmatter. There are 3 different ways you can do so using MCL snippets i.e.
1. Apply at the specific list block using hashtag. This is the recommended option.
2. Apply at the frontmatter. This affects ALL unordered list in that particular note

![](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/hero-mc-list-column-grid-card.png)

{: .note-title }
> Making it work in Live Preview
>
> The column layout will only work on Reading View. If you want to make it work on Live Preview, there are a few options. You can encapsulate the list block in MCL's `[blank-container]` callout
>
> ...
>
> **There's no Markdown Attributes plugin approach**
>
> There are no Markdown Attributes approach due to limitation in specifying at the end of list block


### How To - Using hashtag i.e. `#mcl/list-grid`
Technically List Card is quite similar to List Grid but with extra customisation to make it card like. In order to enable it, place the hashtag anywhere in the top-level list items (preferably in the first bullet for easy identification). There are two options for List Card i.e.
- `#mcl/list-grid` - default minimum width 250px
- `#mcl/list-grid-wide` - default minimum width 350px

If you have consecutive group of list that you actually meant to be a separate lists, ensure to properly "break" it by placing either a header, horizontal line or `<br/>` tag in between

> This option require your Obsidian to be installed with installer version 1.1.9 or higher (note that there are installer and app versions).

Here's an example markdown:
```md
- #### Core Work #mcl/list-grid
    - [[00 Home|Main Goal 1]]
    - [[00 Home|Main Goal 1]]
    - [[00 Home|Main Goal 1]]
        - Collaboration with Jane
    - [[00 Home|Main Goal 1]]
- #### Learning & System
    - [[00 Home|Learning Goal 1]]
    - [[00 Home|Initiative 1]]
    - [[00 Home|Initiative 2]]
- #### Personal
    - [[00 Home|Personal Goal 1]]
    - [[00 Home|Personal Goal 2]]
```

> The number of cards can appear per row is subject to card's minimum width and note's width. Card's minimum width is adjustable via Style Settings plugin.


### How To - Using frontmatter declaration
Using this approach, you will have to specify the css for the column type at the frontmatter (it must be located at the very top of your document, wrapped by two sets of 3 dashes i.e. `---`, see example below for better understanding). MCL provides the following CSS classes
- `two-column-grid-list`
- `three-column-grid-list`

Here's an example markdown:
```md
---
cssclasses: two-column-grid-list
---

- #### Core Work
    - [[00 Home|Main Goal 1]]
    - [[00 Home|Main Goal 1]]
    - [[00 Home|Main Goal 1]]
        - Collaboration with Jane
    - [[00 Home|Main Goal 1]]
- #### Learning & System
    - [[00 Home|Learning Goal 1]]
    - [[00 Home|Initiative 1]]
    - [[00 Home|Initiative 2]]
- #### Personal
    - [[00 Home|Personal Goal 1]]
    - [[00 Home|Personal Goal 2]]
```


## Additional Controls
If you have Style Settings plugin installed, you may control the following aspects (go to `Style Settings > Modular CSS Layout - Multi Column > List Grid and List Card`)
- Card's width and background Color
- Cards' border width and border color
- Gap between card
- Bottom border for the first header in the card

## Example
![example of list grid](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-list-grid.png)
