---
author: "Hugo Authors"
title: "Markdown Syntax Guide"
#date: "2019-03-11"
description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:
  - "markdown"
  - "css"
  - "html"
  - "themes"
categories:
  - "themes"
  - "syntax"
series:
  - "Themes Guide"
aliases:
  - "migrate-from-jekyl"
---


This article offers a sample of basic Markdown syntax that can be used in Hugo content files, also it shows whether basic HTML elements are decorated with CSS in a Hugo theme.
<!--more-->

## Headings

The following HTML `<h1>`—`<h6>` elements represent six levels of section headings. `<h1>` is the highest section level while `<h6>` is the lowest.

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragraph

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

#### Blockquote without attribution

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

#### Blockquote with attribution

> Don't communicate by sharing memory, share memory by communicating.</p>
> — <cite>Rob Pike[^1]</cite>

#### Sometho ther thang

Apple
: A fruit
: multiline style

#### Hugo shortcodes ####

{{/*

THESE DONT WORK :(

 { { %   n o t i c e   n o t e   % } }
 A   n o t i c e   d i s c l a i m e r
 { { %   / n o t i c e   % } }

 { { %   n o t i c e   i n f o   % } }
 A n   i n f o r m a t i o n   d i s c l a i m e r
 { { %   / n o t i c e   % } }

 { { %   n o t i c e   t i p   % } }
 A   t i p   d i s c l a i m e r
 { { %   / n o t i c e   % } }

 { { %   n o t i c e   w a r n i n g   % } }
 A   w a r n i n g   d i s c l a i m e r
 { { %   / n o t i c e   % } }

*/}}

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

Tables aren't part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

|    Name | Age
| ------- | -----
|     Bob | 27
|   Alice | 23
|    Jake | 12
|   CeCee | 99
|   Bruce | 24

### Inline Markdown within tables

| Inline&nbsp;&nbsp;&nbsp;     | Markdown&nbsp;&nbsp;&nbsp;  | In&nbsp;&nbsp;&nbsp;                | Table      |
| -------------------- | --------- | ----------------- | ---------- |
| _italics_, *italics* | **bold**  | ~~strikethrough~~&nbsp;&nbsp;&nbsp; | `code`     |

### Table alignment

| Default Header          | Skip Column | Left Align |          Right Align | Center Align |
| ----------------------- | ----------- | :--------- | -------------------: | :----------: |
| 1                       |             | 3          |                    4 |       5      |

## Code Blocks

### Code block with backticks

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

#### bash

```bash
#!/bin/bash

# Are we being run?
[ "${0}" == "${BASH_SOURCE}" ] && {
    # Oh HELL no
    echo "Non-executable, source file instead"
    exit 1
}
```

#### C

```c
#include <stdlib.h>
#include <stdio.h>

#define  MY_RET  0
#define  MY_NAME "testing"

int main(int argc, char* argv[]) {
    int i = 0;

    printf("%s\n\n", MY_NAME);
    printf("%d:\n", argc);

    for (i = 0; i < argc; ++i) {
        printf("    %d: %s\n", i, argv[i]);
    }

    exit(MY_RET);
}
```

### Code block indented with four spaces

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

### Code block with Hugo's internal highlight shortcode

{{< highlight html >}}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

## List Types

#### Ordered List

1. First item
2. Second item
3. Third item

#### Unordered List

* List item
* Another item
* And another item

#### Nested list

* Item
  1. First Sub-item
  2. Second Sub-item

## Other Elements — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

*[GIF]: Graphics Interchange Format

GIF

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.

