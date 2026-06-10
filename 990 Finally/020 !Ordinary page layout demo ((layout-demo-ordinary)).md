---
date: 2026-05-08
---


This note is in **`991 !!! just my notes`**. There is **no** **`type: article`** and **no** **`tags: paper`** — so you get the **default garden** look: sunflower-friendly layout, **no** automatic blue banners on every **`##`**, and **blockquotes stay blockquotes** (not converted to paper “note” callouts).

## Manual styling {.banner-info}

If you want banner / rounded headings on a **non-paper** page, add classes yourself — this **`##`** line uses **`{.banner-info}`** explicitly.

### Manual rounded box {.rounded-info}

--{.tip}
Explicit **callout** syntax still works on any page: opening line `--{.tip}` and closing `--`.
--

## Default images on a single-column page

On an ordinary page, images are **full width of the content column** unless you override.

![[990 Finally/img/screenshot-020-ordinary-page-layout-demo-layout-demo-ordinary.jpg]]

![[990 Finally/img/screenshot-020-ordinary-page-layout-demo-layout-demo-ordinary.jpg]]{width=2px}

**`{.inline}`** — smaller / natural width (still capped at 100% of the column):

![[990 Finally/img/screenshot-020-ordinary-page-layout-demo-layout-demo-ordinary-2.jpg]]{.inline}

**`{width=…}`**:

![[990 Finally/img/map-020-ordinary-page-layout-demo-layout-demo-ordinary.jpg]]{width=260}

**`{style="…"}`**:

![[990 Finally/img/map-020-ordinary-page-layout-demo-layout-demo-ordinary-2.jpg]]{style="width:45%; max-width:320px; box-shadow:0 2px 8px rgba(0,0,0,.12);"}

## Section-level two columns {.two-col}

Add **`{.two-col}`** on any heading to turn **only** the following chunk into two columns (until the next heading).

Column A: Same image rules — default fills the **half-column** width unless you use **`{.inline}`**, **`width=`**, or **`style=`**.

Column B: **`{.span-cols}`** only “means something” when there are real CSS columns; here it should span **both** section columns.

![[990 Finally/img/screenshot-020-ordinary-page-layout-demo-layout-demo-ordinary-3.jpg]]{.inline}

![[990 Finally/img/cfb7204a873312fed0925ed9e795ac09_MD5.jpg]]{.span-cols}

## Compare with the sibling demo note

Open **`010 Article type layout demo`** in the same folder: same image attributes, but with **automatic paper/article heading treatment** and optional **`dual-column`** in YAML.
