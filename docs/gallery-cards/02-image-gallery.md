---
title: Image Gallery
parent: Gallery Cards
nav_order: 2
---

# Image Gallery
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

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

#### Example
![](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/gallery-callout-langkawi.png)

---

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

#### Example
![](https://raw.githubusercontent.com/efemkay/obsidian-modular-css-layout/main/docs/assets/gallery-cssclass-langkawi.png)

---

## Credits
- Pictures in Gallery example are from Unsplash
	- [@ryaneof](https://unsplash.com/photos/Jh_Xk8RQtG0)
	- [@manish_tulaskar](https://unsplash.com/photos/o0TRwfgXhdw)
	- [@izuddinhelmi](https://unsplash.com/photos/dIArrAUjQV0)
	- [@jaysithutun](https://unsplash.com/photos/0dF2fJjTHCw)
	- [@ramzigraphy](https://unsplash.com/photos/WeiERYmWIT4)
