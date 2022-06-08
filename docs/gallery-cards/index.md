---
title: Gallery Cards
nav_order: 5
has_children: true
---

# Gallery Cards

## Understanding the snippet
- CSS snippet file: [MCL Gallery Cards.css](https://github.com/efemkay/obsidian-modular-css-layout/blob/main/MCL%20Gallery%20Cards.css)
- This snippet will provide the following features
	- Image gallery using callout by specifying the callout-metadata `gallery` e.g. `> [!NOTE|gallery]`
	- Image gallery using YAML/frontmatter .`cssClass: image-gallery`
	- Dimension control for images in bullet list
	- Image Zoom

## Image Gallery Using Callout
- Transcluded/embedded images will be stacked side by side. Add empty lines in between the images to create new row

```markdown
> [!blank-container|no-margin gallery] Title
>
> ![[path/to/pic1.jpg]]
> ![[path/to/pic2.jpg]]
>
> ![[path/to/pic3.png]]
> ![[path/to/pic4.png]]
> ![[path/to/pic5.png]]
```

## Image Gallery Using YAML `cssClass: image-gallery`
- Specify the following frontmatter at the very top of your markdown notes
- Similar to using callout, transcluded/embedded images will be stacked side by side. Add empty lines in between the images to create new row


```markdown
---
cssClass: image-gallery
---

![[path/to/pic1.jpg]]
![[path/to/pic2.jpg]]

![[path/to/pic3.png]]
![[path/to/pic4.png]]
![[path/to/pic5.png]]

```

## Dimension control for images in bullet list
- By default, this feature is **enabled** when you apply the snippet. To disable, go to Style Settings and under `Modular CSS Layout - Gallery Cards > Image and Gallery Settings` enable the "Disable Image Control in Lists"

## Image Zoom
- To enable this feature, go to Style Settings and under `Modular CSS Layout - Gallery Cards > Image and Gallery Settings` enable the "Enable Image Zoom via CSS in Lists"
