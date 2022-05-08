---
cssclass: wide-page
---

> [!multi-column]
> > [!Todo]+ Deliverables Milestone
> > - [x] Insider's Alpha Release
> > - [ ] Gold & Silver Supporters Meetup
> > - [ ] Public Beta Release
> 
> > [!Summary]+ Funding Milestone
> > - Series A: $ 1.1 mil
> > - Series B: ongoing
> > - Series C: planned

## Project Background
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Interdum velit euismod in pellentesque massa placerat duis. Bibendum arcu vitae elementum curabitur vitae nunc. Quis ipsum suspendisse ultrices gravida. Risus in hendrerit gravida rutrum quisque non tellus.

#### Use Case
Viverra mauris in aliquam sem fringilla ut morbi tincidunt. Faucibus pulvinar elementum integer enim neque volutpat ac tincidunt vitae. Urna et pharetra pharetra massa massa ultricies. Ultrices eros in cursus turpis massa tincidunt. Ullamcorper velit sed ullamcorper morbi. Ornare quam viverra orci sagittis eu. Tortor dignissim convallis aenean et tortor at.
- Consectetur adipiscing elit ut aliquam purus sit amet luctus.
- Est lorem ipsum dolor sit. Blandit cursus risus at ultrices mi.
- Vestibulum mattis ullamcorper velit sed ullamcorper. In mollis nunc sed id semper risus in.
{.two-column-list-block}

## Supporters
- **Nina** (Gold)
- **Frankie** (Silver)
- **Nurul** (Silver)
- **Kamala** (Silver)
- Nguyen
- Cypher
- Powell
- Sam
- Kate
- Roger
- Sharon
- Peter
- Obadiah
- Serena
- Nicholas
{.multi-column-list-block}

---

> [!NOTE]+ How to achieve the look?
> - This note layout will require the following snippet and plugin
> 	- `MCL Multi Column.css` css snippet for the multi-column callout,
> 	- [Markdown Attributes](https://github.com/valentine195/obsidian-markdown-attributes) plugin for the multi-column unordered list, and
> 	- Optional. `MCL Wide Views.css` css snippet for the wide-page view
> - To get the multi-column callout, use `[!multi-column]` custom callout and nest two standard callouts (i.e. `[!todo]` and `[!summary]`) within it.
> 	- Ensure that these nested callout has double angle bracket (`>>`) to indicate they are nested within and the spacing between the nested callout have only single angle bracket (`>`)
> - To get the multi-column unordered list, type `{.multi-column-list-block}` on a new line immediately after the last bullet.
> 	- Using Style Settings plugin, set the **MCL - Multi Column > List Column Settings > Minimum Column Width** to 100px (if you want to have at least two columns in mobile phone view, else just leave it at default (200px)).
> 	- Note that this multi column list will not render in editing view (not even in live preview mode). It will also require Markdown Attributes plugin installed and enabled.

> [!Warning]+ Potential Issues
> - Markdown won't render properly if the multi-column list has a sublist (2nd level indent list) as the very end.
> 	- This is due to Markdown Attributes plugin require it to be on the new line immediately after the list, but Obsidian will be confused with two level indent followed by non-bullet text.
> - Box shadown on certain themes may look a bit off for a sharp eye.
> 	- Some theme heavily customise their callout, as such you may notice that box shadow does not appear round on the inner border (that are facing another sub-callout, for theme that uses border-radius features).

