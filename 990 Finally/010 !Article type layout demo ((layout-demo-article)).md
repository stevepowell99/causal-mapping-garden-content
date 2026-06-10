---
type: article
tags:
  - dual-column
date: 2026-05-08
---

This note lives in **`991 !!! just my notes`**. It uses **`type: article`** (same effect as **`tags: paper`**): working-paper shell, serif body, no flower icon, and automatic **`##`** / **`###`** / blockquote styling. **`dual-column`** is also set so the **main body is two columns** on the web and in PDF-style layout; **`paper`** PDFs would add columns anyway, but this makes the HTML match.

## What you should see on this page

This **`##`** heading was plain in Markdown; the build added the blue **banner-info** style. The next line is a **`###`** heading — it should get the soft **rounded-info** box.


### Subsection (automatic `rounded-info`)

> On **`article` / `paper`** pages, a normal blockquote like this one is turned into a **note** callout (not a tip).

### Images when the page really has two columns

Without any extra attributes, an image should stay **inside one column** (narrow band), not span the whole content area.

![](img/959605bb2315635037984e235082bc14_MD5.jpg)

**`{.span-cols}`** — use this when you want the figure to **break out and span both columns**:

![](img/screenshot-010-article-type-layout-demo-layout-demo-article.jpg){.span-cols}

**`{.inline}`** — keeps the image from being forced to full column width; handy for logos or small figures inside text.

![](img/screenshot-010-article-type-layout-demo-layout-demo-article-2.jpg){.inline}

**`{width=…}`** — passed through as the HTML `width` attribute (simple sizes):

![](img/screenshot-010-article-type-layout-demo-layout-demo-article-3.jpg){width=200}

**`{style="…"}`** — full CSS control (units, `max-width`, etc.):

![](img/map-010-article-type-layout-demo-layout-demo-article.jpg){style="width:32%; max-width:240px; border:2px solid #ccc; border-radius:6px;"}

## Section-only two columns `{.two-col}`

This heading has **`{.two-col}`** in the source. Content below runs in **two columns until the next heading**, even on a page that already uses page-level columns (use sparingly — it is easy to get a “columns inside columns” look).

Left column text: Lorem ipsum dolor sit amet.

Right column text: Consectetur adipiscing elit.

![](img/map-010-article-type-layout-demo-layout-demo-article-2.jpg){.inline}

## Done

That covers **article-type defaults**, **page-level two columns**, **`{.span-cols}`**, **`{.inline}`**, **`width=`**, **`style=`**, and a **`{.two-col}`** segment.
