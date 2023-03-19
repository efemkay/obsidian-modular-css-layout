---
title: Image Float (Left/Right)
parent: Gallery Cards
nav_order: 4
---

# Image Float
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Float Left/Right in Reading View Only
- Use this syntax to enable image float in Reading View only. In Live Preview it will be displayed on different lines
- Syntax: `![[<imagefile.jpg>|<position>|<size>]]`
- Example: `![[ryaneof-Jh_Xk8RQtG0-unsplash.jpg|right|300]]`

## Float Left/Right in Live Preview and Reading View
- Use this syntax to enable image float in both Live Preview and Reading View. In case you didn't notice, the difference is just prepending `float-` before the position.
- Syntax: `![[<imagefile.jpg>|float-<position>|<size>]]`
- Example: `![[ryaneof-Jh_Xk8RQtG0-unsplash.jpg|float-right|300]]`

> Note that editing float in Live Preview will be a bit off (or "janky"). Navigate using keyboard instead of mouse/trackpad. Even better use Source Mode.


## External Images
Technically, the image float positioning can work with external link images but it is currently not aesthetically optimised (in term of gaps and other adjustment).

I will update this in the future. But if you must use it now, the syntax is `![<position>|<size>](<imagefile.jpg>)` and `![float-<position>|<size>](<imagefile.jpg>)`
