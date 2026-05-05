---
title: "Markdown Guide"
date: 2026-05-05
draft: false
description: "A reference of all native Markdown syntax elements."
tags: ["markdown", "guide", "syntax", "reference"]
---

# Markdown Syntax Reference

## Headings

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

---

## Paragraphs & Line Breaks

This is a paragraph. Paragraphs are separated by a blank line.

This is a second paragraph. To create a hard line break,  
end a line with two or more spaces, then press Return.

---

## Emphasis

*This text is italic using asterisks.*  
_This text is italic using underscores._

**This text is bold using asterisks.**  
__This text is bold using underscores.__

***This text is bold and italic.***  
___This text is also bold and italic.___

~~This text has strikethrough.~~

---

## Blockquotes

> This is a blockquote.

> Blockquotes can span multiple paragraphs.
>
> Just add a `>` on the blank line between them.

> Blockquotes can be nested.
>
> > This is a nested blockquote.
> >
> > > And nested even deeper.

---

## Lists

### Unordered Lists

- Item one
- Item two
  - Nested item
  - Another nested item
    - Deeply nested item
- Item three

* Asterisks also work
* For unordered lists

+ As do plus signs
+ Like this

### Ordered Lists

1. First item
2. Second item
   1. Nested ordered item
   2. Another nested ordered item
3. Third item
4. The actual numbers don't matter to Markdown
1. It just needs to start with a number

### Task Lists

- [x] Write the markdown reference post
- [x] Include all syntax elements
- [ ] Publish to Hugo blog
- [ ] Share with the world

---

## Code

### Inline Code

Use backticks for `inline code`, like referencing a `variable` or a `function()`.

### Fenced Code Blocks

```
This is a plain fenced code block with no language specified.
```

```bash
# Bash example
echo "Hello, Hugo!"
for i in 1 2 3; do
  echo "Item $i"
done
```

```javascript
// JavaScript example
const greet = (name) => {
  return `Hello, ${name}!`;
};

console.log(greet("World"));
```

```python
# Python example
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

print(list(fibonacci(10)))
```

```html
<!-- HTML example -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Example</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
  </body>
</html>
```

```css
/* CSS example */
body {
  font-family: sans-serif;
  line-height: 1.6;
  color: #333;
}
```

### Indented Code Block

    This is an indented code block.
    It uses four spaces of indentation.
    No language highlighting is applied.

---

## Horizontal Rules

Three or more hyphens:

---

Three or more asterisks:

***

Three or more underscores:

___

---

## Links

### Inline Links

[Visit Hugo's website](https://gohugo.io)

[Hugo website with a title](https://gohugo.io "The world's fastest framework for building websites")

### Reference Links

[Hugo][hugo-ref] is a fast static site generator.

[Markdown][md-ref] is a lightweight markup language.

[hugo-ref]: https://gohugo.io "Hugo - The world's fastest framework for building websites"
[md-ref]: https://daringfireball.net/projects/markdown/

### Autolinks

<https://gohugo.io>

<hello@example.com>

---

## Images

### Inline Image

![Markdown logo](https://markdown-here.com/img/icon256.png "Markdown Logo")

### Reference Image

![Alt text][image-ref]

[image-ref]: https://markdown-here.com/img/icon256.png "Markdown Logo via reference"

---

## Tables

| Column One   | Column Two   | Column Three  |
| ------------ | ------------ | ------------- |
| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3  |
| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3  |
| Row 3, Col 1 | Row 3, Col 2 | Row 3, Col 3  |

### Aligned Columns

| Left-aligned | Center-aligned | Right-aligned |
| :----------- | :------------: | ------------: |
| Left         |    Center      |         Right |
| Text         |    Text        |          Text |
| More text    |   More text    |     More text |

---

## Footnotes

Here is a sentence with a footnote.[^1]

And another sentence with a second footnote.[^note]

[^1]: This is the first footnote.
[^note]: This is a named footnote. Footnote text can span multiple lines  
         as long as subsequent lines are indented.

---

## Definition Lists

*(Supported by many Markdown processors and Hugo)*

Term One
: Definition for term one.

Term Two
: First definition for term two.
: Second definition for term two.

---

## Escaping Characters

Markdown reserves certain characters. Use a backslash `\` to escape them:

\* Not italic \*  
\*\* Not bold \*\*  
\# Not a heading  
\[Not a link\](https://example.com)  
\`Not inline code\`  
\> Not a blockquote  
\- Not a list item  
\. Not an ordered list  

Full list of escapable characters: `\ ` * _ { } [ ] ( ) # + - . !`

---

## HTML in Markdown

Native Markdown allows inline HTML. Hugo may render or sanitize this depending on your `config.toml` settings.

<p>This is a raw HTML paragraph.</p>

<details>
  <summary>Click to expand a details block</summary>
  <p>This content is hidden until expanded.</p>
</details>

<mark>This text is highlighted using the HTML mark element.</mark>

<kbd>Ctrl</kbd> + <kbd>C</kbd> — keyboard key styling via `<kbd>`.

<sup>Superscript</sup> and <sub>Subscript</sub> via HTML tags.

---

## Putting It All Together

Here's a short sample that combines multiple elements naturally:

> **Note:** The following is a demonstration combining **bold**, *italic*, `inline code`, and a [link](https://gohugo.io).

A table with mixed content:

| Feature       | Supported | Notes                          |
| :------------ | :-------: | :----------------------------- |
| Headings      | ✅        | Six levels                     |
| Bold / Italic | ✅        | Asterisks or underscores       |
| Tables        | ✅        | GFM-style                      |
| Footnotes     | ✅        | Requires Goldmark or extension |
| Task Lists    | ✅        | GitHub Flavored Markdown       |
| HTML          | ✅        | Enable `unsafe` in config      |
