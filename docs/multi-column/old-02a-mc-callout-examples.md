

### Standard Multi-Column Callout
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

### Icon Links Dashboard using Fixed Width option
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

### Example Screenshot - Multi Column Callout with Width Control
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-width-control.png" height="350px" />

---

### Using Multi-Column Callout within another Multi-Column Callout

![example of list column](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/mc-callout-within-mc-callout.jpg)

```
> [!multi-column]
>
> > [!blank|no-margin pw2]
> > Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
>
> > [!multi-column|pw6]
> >
> > > [!tldr]- Manifest
> > > Contents
> >
> > > [!info]- Backlog
> > > Contents
> >
> > > [!tip] Project
> > > - ### Project A
> > > 	- completed
> > > - ### Project B
> > > 	- ongoing
```

- It will be easier if we think how to build this logically. Remember, in the above example, the main `[!multi-column]` contains two children i.e. `[!blank|no-margin pw2]` and `[!multi-column|pw6]`.
- The second (or nested `[!multi-column|pw6]`) then contains three (3) sub-callouts i.e. `[!tldr]- Manifest`, `[!info]- Backlog` and `[!tip] Project`

{: .note-title }
> Sub-callout hierarchy for example above
>
> - `[!multi-column]`
> 	1. `[!blank|no-margin pw2]`
> 	2. `[!multi-column|pw6]`
> 		1. `[!tldr]- Manifest`
> 		2. `[!info]- Backlog`
> 		3. `[!tip] Project`


---

### Example GIF - Install the snippet and apply Multi Column Callout
<img src="https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/how%20to%20install%20and%20enable%20MCL.gif" height="350px" />
