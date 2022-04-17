# Modular CSS Layout for Obsidian.md
This is a repository for modular CSS layout hack for use with [Obsidian.md](https://obsidian.md/). It's meant to complement/assist Community Theme, focusing solely on providing alternative layout to standard width and standard top-bottom block view.

To use, download or copy the css into your `[vault]/.obsidian/snippets` folder and enable them in Settings > Appearance > CSS snippets.

## Wide Views
> [css snippet here](https://github.com/efemkay/obsidian-css-layout/blob/main/page%20width%20and%20wide%20views.css)

This snippet allow you to use cssclasses to enable either wide views - either wide-page, wide-dataview, wide-table or combination of those. For this snippet to works, you will need to disable "Readable line length" in `Settings > Editor`.

For wide-dataview and wide-table, you will need to install [Contextual Typography](https://github.com/mgmeyers/obsidian-contextual-typography) plugin.

<img src="https://user-images.githubusercontent.com/42369515/163697717-911d36b3-f505-49c2-803b-775f1d7fae9a.png" height="350px">


## Multi Column Views
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
	- `two-column-grid-list`
	- `three-column-grid-list`

`xx-column-list` uses CSS Column property where it will flow from top to bottom but spreading the list evenly between the number of columns (like how newspaper paragraph works)

`xx-column-grid-list` uses CSS Grid layout where it will try to position top level list (bullet) from left to right (with sub-list behaving per normal (from top to bottom). In the case where the screen is too small, it will revert to stacking (top to bottom)

<img src="https://user-images.githubusercontent.com/42369515/163700640-245e4275-f329-4cb2-9138-07cb276354cc.png" height="350px">

## Support
I do this on my free time for personal joy. However, a cup of coffee or two would motivate me further! If you like what I do, and want to contribute back, you can support me via Ko-fi

<a href='https://ko-fi.com/M4M3C77PF' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
