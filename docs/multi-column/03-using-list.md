---
title: Using List
parent: Multi Column
nav_order: 3
---

# MC Using (Unordered) List
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Using (Unordered) List with Markdown Attributes plugin
- css classes available
	- `two-column-list`
	- `three-column-list`
	- `multi-column-list-block` -- require Markdown Attributes plugin
	- `two-column-grid-list`
	- `three-column-grid-list`

`<two|three|multi>-column-list` uses CSS Column property where it will flow from top to bottom but spreading the list evenly between the number of columns (like how newspaper paragraph works). The helper class must be put in the YAML (frontmatter) section and will apply to all first level list in the note.

Meanwhile `{.<two|three|multi>-column-list-block}` can be applied at list-block level (example as per below) but require J Valentine's [Markdown Attributes](https://github.com/valentine195/obsidian-markdown-attributes) plugin. This will allow only certain list be subject to column layout while others remain unchanged.
```markdown
- item a
- item b
- item c
- item d
{.two-column-list-block}
```

`<two|three>-column-grid-list` uses CSS Grid layout where it will try to position top level list (bullet) from left to right (with sub-list behaving per normal (from top to bottom). In the case where the screen is too small, it will revert to stacking (top to bottom). The helper class must be put in the YAML (frontmatter) section and will apply to all first level list in the note.

<img src="https://user-images.githubusercontent.com/42369515/163700640-245e4275-f329-4cb2-9138-07cb276354cc.png" height="350px">

> to get multi column list view in Live Preview, you can wrap it inside a `[!blank-container]` callout


## Using (Unordered) List with Contextual Typography plugin
- This option will utilise tags (instead of css classes)
	- `#mcl/list-column` -- require Contextual Typography plugin
	- `#mcl/list-grid` -- require Contextual Typography plugin
	- `#mcl/list-card` -- require Contextual Typography plugin

This option will allow you to create multi column lists on block basis and compatible for list with sublist (which will not work well for Markdown Attributes plugin)

Place the tag anywhere in the lists (preferably in the first bullet for easy identification). If you have consecutive group of list that you actually meant to be a separate lists, ensure to properly "break" it by placing either a header, horizontal line or `<br/>` tag in between

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

Using this option, the number of columns or grids or cards is determined by minimum width (adjustable using Style Settings plugin), available note/page width and how many bullets. Under default settings, normal page layout can fit 3 columns/grids/cards but if there's only two bullets, it will expand to fill the space.
