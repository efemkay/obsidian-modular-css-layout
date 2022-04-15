# obsidian-css-layout
This is repository for CSS Layout hack for use with [Obsidian.md](https://obsidian.md/).

## Page Width and Wide Views
> [css snippet here](https://github.com/efemkay/obsidian-css-layout/blob/main/page%20width%20and%20wide%20views.css)

This snippet allow you to use cssclasses to enable either wide views - either wide-page, wide-dataview, wide-table or combination of those. For this snippet to works, you will need to disable "Readable line length" in `Settings > Editor`.

For wide-dataview and wide-table, you will need to install [Contextual Typography](https://github.com/mgmeyers/obsidian-contextual-typography) plugin.

## Multi Column Views
### Using Callout
- Custom Callout available
	- `> [!three-column]`
	- `> [!two-column]`
	- `> [!blank-container]`

This layout take advantage of the new Obsidian Callout feature. Using the callout as parent 'div' to house the sub callout.

Once you enabled the css snippet, you use this feature by creating a custom callout like example below

~~~markdown
> [!three-column]
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

### Using (Unordered) List
- css classes available
	- `two-column-list`
	- `three-column-list`
	- `two-column-grid-list`
	- `three-column-grid-list`

`xx-column-list` uses CSS Column property where it will flow from top to bottom but spreading the list evenly between the number of columns (like how newspaper paragraph works)

`xx-column-grid-list` uses CSS Grid layout where it will try to position top level list (bullet) from left to right (with sub-list behaving per normal (from top to bottom). In the case where the screen is too small, it will revert to stacking (top to bottom)
