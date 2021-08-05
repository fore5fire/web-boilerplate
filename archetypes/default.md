---
# This is the page front-matter, which uses YAML syntax
# (https://www.lzone.de/cheat-sheet/YAML).

# title is how the page name is shown in the menu or in a list page.
title: "{{ replace .Name "-" " " | title }}"
# Change draft to true to hide this page from the published website. This lets
# you start new  pages without needing to finish them right away or save them
# somewhere else.
draft: false
# Remove menu if you don't want your page to show up directly in the navigation
# bar.
menu: main
# Weight determines how this page is ordered on the menu or in list pages.
# Remove it to use alphabetical ordering by title.
weight: 100
---

## Page Content

Everything after the front-matter is the page content written in Markdown.
Here's a quick cheat-sheet copied from
https://www.markdownguide.org/cheat-sheet:

````
Heading         # H1
                ## H2
                ### H3
Bold            **bold text**
Italic          *italicized text*
Blockquote      > blockquote
Ordered List    1. First item
                2. Second item
                3. Third item
Unordered List  - First item
                - Second item
                - Third item
Preformatted    `this won't be interpreted as markdown or HTML`
Link            [title](https://www.example.com)
Image           ![alt text](image.jpg)

Horizontal Rule
---

Table:
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

Preformatted Block
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

Footnote
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

Definition List term
: definition

Strikethrough
~~The world is flat.~~

Task List
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
````