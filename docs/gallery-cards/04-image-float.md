---
title: Float Image
parent: Gallery Cards
nav_order: 4
---

# Float Image
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Overview

Float Image is similar to Float Callout but apply directly to the images (doesn't require you to wrap it in a callout). Currently it uses image caption to identify how you want to float it, but in the future I intend to make it work with anchor tag `#` as well.

### How to Use / Basic Syntax

1. Add your image (either internal or external) as per normal
2. Add `left` or `right` to the image caption (similar to markdown display text i.e. `|`) e.g. `![[image.jpg|right]]`

> You can still specify image width per normal if you desire, just make sure the width is the last syntax before closing bracket `]]`, e.g. below
>
> `![[ryaneof-Jh_Xk8RQtG0-unsplash.jpg|right|300]]`

Here's an example markdown

```markdown
### Main Article

![[ryaneof-Jh_Xk8RQtG0-unsplash.jpg|right|350]]

Content of the main article
```



## Additional Controls (and Notes)

### Apply to Live Preview

By default, if you only specify either `left` or `right`, Float Image will only work in Reading View. If you want it to also work in Live Preview, prepend `float-` before the `left` or `right` e.g. `![[image.jpg|float-right]]`

Here's an example markdown

```markdown
## Main Article

![[ryaneof-Jh_Xk8RQtG0-unsplash.jpg|float-right|350]]

Content of the main article
```

> **Note on Editing in Live Preview**
>
> In previous version of Float Image, editing text next to it was quite janky. I've improved it a bit (for `float-right` at least). For `float-left` you may still find selecting and navigating the text (up and down) still not possible.
>
> To edit, it's better to navigate using keyboard (from the top or bottom) instead of mouse/trackpad. Even better, use Source Mode to edit.


### External Images

Technically, the image float positioning can work with external link images but it is currently not aesthetically optimised (in term of gaps and other adjustment).

I will update this in the future. But if you must use it now, the syntax is `![<position>|<size>](<imagefile.jpg>)` and `![float-<position>|<size>](<imagefile.jpg>)`
