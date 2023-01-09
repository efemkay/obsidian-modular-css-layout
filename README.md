# Modular CSS Layout for Obsidian

![](https://img.shields.io/github/v/release/efemkay/obsidian-modular-css-layout) ![](https://img.shields.io/github/release-date/efemkay/obsidian-modular-css-layout) ![](https://img.shields.io/github/license/efemkay/obsidian-modular-css-layout) ![](https://img.shields.io/github/downloads/efemkay/obsidian-modular-css-layout/total)

> - Fixes for Breadcrumbs plugin and list columns bullet alignment

This is a repository for modular CSS layout hack for use with [Obsidian.md](https://obsidian.md/). It's meant to complement/assist Community Theme, focusing solely on providing alternative layout to standard width and standard top-bottom block view.

I mainly do casual test on select popular themes like ITS, Primary, Shimmering Focus, Prism, and Minimal. Need your help to let me know if there's anything not working right. Do log in [MCL GH Issue](https://github.com/efemkay/obsidian-modular-css-layout/issues) if you find anything not working properly.

### Table of Content
- [Install/Download](#installation--download-and-enable)
- [Wide Views](#wide-views)
- [Multi Column](#multi-column)
- [Gallery Cards](#gallery-cards)
- [Support Me](#support-me)

## Installation / Download and Enable

This is actually just a CSS code snippets collection. So it isn't an installation per se, but rather download and enable in Obsidian. The best way is to use Mara Li's [Snippet Downloader](https://github.com/Mara-Li/obsidian-snippet-downloader) plugin as I have plans to update this snippets from time to time


## Wide Views
> CSS snippet: `MCL Wide Views.css`

> This section only briefly explains Wide Views snippet. Please go through the documentation site [Wide Views - Modular CSS Layout](https://efemkay.github.io/obsidian-modular-css-layout/wide-views/) for more details.

This snippet provides you the following features:
- Full width page or blocks (dataview, table and backlinks) per page/note basis by specifying custom `cssClass` at the frontmatter (YAML)
	- `wide-page`
	- `wide-dataview` -- require Contextual Typography plugin
	- `wide-table` -- require Contextual Typography plugin
	- `wide-callout`
	- `wide-backlinks`
	- vault-wide toggle for each of the above
- Narrow width page per page/note basis for vault with RLL disabled by specifying custom `cssClass` at the frontmatter (YAML)
    - `narrow-page`
- Adjustable RLL (custom css class toggle) applicable to entire vault
    - Disabled by default. Enable it via Style Settings plugin

> For wide-dataview and wide-table, you will need to install [Contextual Typography](https://github.com/mgmeyers/obsidian-contextual-typography) plugin.


#### Example

```markdown
---
cssClass: wide-page
---

<the rest of your note>
```

<img src="https://user-images.githubusercontent.com/42369515/163697717-911d36b3-f505-49c2-803b-775f1d7fae9a.png" height="350px">


## Multi Column
> CSS snippet: `MCL Multi Column.css`

> This section only briefly explains Multi Column snippet. Please go through the documentation site [Multi Column - Modular CSS Layout](https://efemkay.github.io/obsidian-modular-css-layout/multi-column/) for more details.


This snippet provides you the following features:


- Multi column layout using Callout
	- `> [!multi-column]`
	- `> [!blank-container]`
- Multi column layout using (Unordered) List
    - it can be done via custom `cssClass` at the frontmatter
        - `two-column-list`
        - `three-column-list`
        - `two-column-grid-list`
        - `three-column-grid-list`
    - it can also be done at block level (inside your note)
        - `multi-column-list-block` -- require Markdown Attributes plugin
- Multi column layout using (Unordered) List AND tag (instead of css classes)
	- `#mcl/list-column` -- require Contextual Typography plugin
	- `#mcl/list-grid` -- require Contextual Typography plugin
	- `#mcl/list-card` -- require Contextual Typography plugin
- Side / Floating Column using Callout
    - `> [!<anycallout>|<left|right>-<small|medium|large>]`
    - `> [!blank-container||<left|right>-<small|medium|large>]`


#### Example Multi Column using Callout
```markdown
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

<img src="https://user-images.githubusercontent.com/42369515/163700561-c8d62aa3-0ac8-488c-a80e-8bfb3b539ca8.png" height="350px" >

#### Example Multi Column using List
<img src="https://user-images.githubusercontent.com/42369515/163700640-245e4275-f329-4cb2-9138-07cb276354cc.png" height="350px">


## Gallery Cards
> CSS snippet: `MCL Gallery Cards.css`

> This section only briefly explains Gallery Cards snippet. Please go through the documentation site [Gallery Cards - Modular CSS Layout](https://efemkay.github.io/obsidian-modular-css-layout/gallery-cards/) for more details.

This snippet provides you the following features:
- Image gallery using callout by specifying the callout-metadata `gallery` e.g. `> [!NOTE|gallery]`
- Image gallery using YAML/frontmatter .`cssClass: image-gallery`
- Image and Mermaid Diagram Controls
	- Dimension control for images in bullet list
	- Image Zoom
	- Mermaid Scale and Zoom


## Support Me
I do this on my free time for personal joy. However, a cup of coffee or two would motivate me further! If you like what I do, and want to contribute back, you can support me via Ko-fi

<a href='https://ko-fi.com/M4M3C77PF' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
