# Modular CSS Layout for Obsidian.md
`v0.2.0 updated 2022-05-29`

This is a repository for modular CSS layout hack for use with [Obsidian.md](https://obsidian.md/). It's meant to complement/assist Community Theme, focusing solely on providing alternative layout to standard width and standard top-bottom block view.

### Table of Content
- [Wide Views](https://github.com/efemkay/obsidian-modular-css-layout#wide-views)
- [Multi Column](https://github.com/efemkay/obsidian-modular-css-layout#multi-column)
    - [Using Callout](https://github.com/efemkay/obsidian-modular-css-layout#using-callout)
    - [Using (unordered) list](https://github.com/efemkay/obsidian-modular-css-layout#using-unordered-list)
    - [Side Column / Floating Column](https://github.com/efemkay/obsidian-modular-css-layout#side-column--floating-column)
- [Support Me](https://github.com/efemkay/obsidian-modular-css-layout#support-me)

## How to use / install?
To use, download or copy the css into your `[vault]/.obsidian/snippets` folder and enable them in Settings > Appearance > CSS snippets.
Since I'm planning to update this snippets from time to time, you can use Mara Li's [Snippet Downloader](https://github.com/Mara-Li/obsidian-snippet-downloader) plugin to use Obsidian interface to download and update the snippets (when update is available).

## Wide Views
- CSS snippet: `MCL Wide Views.css`
- Custom CSS class available
	- `wide-page`
	- `wide-dataview` -- require Contextual Typography plugin
	- `wide-table` -- require Contextual Typography plugin
	- `wide-backlinks`
    - `narrow-page`
- Custom CSS class toggle available
    - Adjustable RLL (via Style Settings plugin)

This snippet allow you to use Obsidian CSS class helper to enable any of the wide views. To use it, add the helper class in the YAML (frontmatter) of your note (which must be at the top of the note) like below.

```markdown
---
cssClass: wide-page
---

<the rest of your note>
```

For wide-dataview and wide-table, you will need to install [Contextual Typography](https://github.com/mgmeyers/obsidian-contextual-typography) plugin.

<img src="https://user-images.githubusercontent.com/42369515/163697717-911d36b3-f505-49c2-803b-775f1d7fae9a.png" height="350px">


## Multi Column
### Using Callout
- Custom Callout available
	- `> [!multi-column]`
	- `> [!blank-container]`

This layout take advantage of the new Obsidian Callout feature. Using the callout as parent 'div' to house the sub callout. You can nest as many sub-callouts/dataview codeblocks within the [!multi-column] callout - it will create a sub-callout/dataview renders with minimum width of 200px (can be change using Sytle Settings plugin). The sub-callout/dataview renders will expand if [!multi-column] has extra space or overflow to next row if it doesn't.

Once you enabled the css snippet, you use this feature by creating a custom callout like example below

~~~markdown
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
~~~
> note that when you insert callout within callout, the line separating the callouts should only use single angle bracket (">")

<img src="https://user-images.githubusercontent.com/42369515/163700561-c8d62aa3-0ac8-488c-a80e-8bfb3b539ca8.png" height="350px" >


### Using (Unordered) List
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

### Side Column / Floating Column
- Using Callout metadata
	- `> [!{anycallout}|{left|right}-{small|medium|large}]`
	- `> [!blank-container||{left|right}-{small|medium|large}]`

example
`> [!warning|right-small]`

## Support Me
I do this on my free time for personal joy. However, a cup of coffee or two would motivate me further! If you like what I do, and want to contribute back, you can support me via Ko-fi

<a href='https://ko-fi.com/M4M3C77PF' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
