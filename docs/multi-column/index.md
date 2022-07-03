---
title: Multi Column
nav_order: 4
has_children: true
---

# Multi Column

## Understanding the snippet
- CSS snippet file: [MCL Multi Column.css](https://github.com/efemkay/obsidian-modular-css-layout/blob/main/MCL%20Multi%20Column.css)
- This snippet will provide the following features
	- Multi column layout using custom callout `[!multi-column]`
		- to be used with sub callout or codeblocks
	- Invisible container using custom callout `[!blank-container]`
		- to be used as grouping container like a dashboard
	- Multi column bullet list at (a) note level, and (b) block level
	- Side/Floating column using callout-metadata `<left|right>`


## Using Callout
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

### Width Control
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

#### Example Screenshot - Multi Column (general)
<img src="https://user-images.githubusercontent.com/42369515/163700561-c8d62aa3-0ac8-488c-a80e-8bfb3b539ca8.png" height="350px" />

#### Example Screenshot - Multi Column Callout Width Control
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-width-control.png" height="350px" />

#### Example GIF
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/how%20to%20install%20and%20enable%20MCL.gif" height="350px" />

## Using (Unordered) List
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

## Side Column / Floating Column
- Using Callout metadata
	- `> [!<anycallout>|<left|right>-<small|medium|large>]`
	- `> [!blank-container|<left|right}-<small|medium|large>]`

example
`> [!warning|right-small]`
