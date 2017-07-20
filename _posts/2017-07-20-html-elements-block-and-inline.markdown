---
layout: post
title: "HTML Elements: Block & Inline"
tags:
date: 2017-07-20T18:25:02-05:00
---
## HTML Structure
```
<!DOCTYPE html>
<html>
  <head>
    <title>Web page #1!</title>
  </head>
  <body>
    <h1>My first web page</h1>
    <h2>Written with the guidance of Epicodus</h2>

    <p>This is my first web page!</p>
    <p>Isn't it nice?</p>

    <p>Here are some things I'm going to learn about coding:</p>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
      <li>And a lot more!</li>
    </ul>
  </body>
</html>
```
The `<!DOCTYPE html>` tag tells the browser that this document contains HTML, and specifically that it contains the newest version of HTML, HTML5. (An example of a doctype for an older version of HTML is `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">`.)

The `<head>` tag contains information about the page, which for now is just the `<title>` tag. The `<title>` tag sets the title for the web page - if you look in your browser, you can see that the title of the browser tab is now _Web page #1!_.

The actual content of the page is wrapped in a `<body>` tag.

### Indentation & Whitespace
In HTML, the beginning and ending tags of an element on multiple lines should always be left-aligned. For example, when you see `<html>`, you should be able to visually scan the page straight down to find its closing tag (the same for `<head>` and `<body>`). One way to implement this is to create opening and closing tags at the same time and then add the contents.

When elements are nested within another element, they should be indented two spaces from the opening tag. For example, `<head>` is indented two spaces from `<html>` and `<title>` is indented two spaces from `<head>`.

## Block Elements
****
### Terminology
- **Block elements:** HTML elements that create a "block" in the display by appearing on their own line.
- **Tags:** HTML annotations which indicate how the text should be formatted.
- **P tag:** An HTML tag that indicates text should be formatted in a paragraph.
- **Opening tag:** An HTML tag that appears before the text that will be formatted in an HTML document. For example, the `<p>` in `<p> This is a paragraph. </p>` is the opening tag.
- **Closing tag:** An HTML tag that appears after the text that is formatted. It matches the opening tag but begins with a /. For example, the `</p>` in `<p> This is a paragraph. </p>` is the closing tag.
- **End tag:** An alternative name for a closing tag.
- **Header:** An HTML tag to indicate the text being formatted is a header. There are 6 sizes of HTML headers `<h1>` through `<h6>`.
- **Whitespace:** All of the "empty" space that includes spaces, indentation, blank lines, etc.
- **Unordered list:** A list of items that are designated with bullet points.
- **Ordered list:** A list of items designated with numbers.
- **List item:** An item in an ordered or unordered list.

### HTML block Element Tags
- `<head>`: Head
- `<body>`: Body
- `<p>`: Paragraph
- `<ul>`: Unordered list
- `<li>`: List item (must exist within a set of `<ul>` or `<ol>` tags)
- `<ol>`: Ordered list
- `<h1>` through `<h6>`: Headings
- `<title>`: Title

## Inline Elements
****
### Terminology
- **Inline element:** HTML elements that do not appear on their own line, but instead share a line with other elements.
- **Attribute:** Additional information provided to an HTML tag. For instance, the href attribute in an `<a>` tag provides the URL a link should travel to.
- **Relative path:** A path to a file within the project itself. Usually referring to the location provided in as the href attribute in an `<a>` tag.
- **Self-closing:** An HTML element that does not require a closing tag, such as `<img>`.

### Inline Elements
- `<strong>`: Makes text appear bolder. Example: `<strong>This content is important.</strong>`
- `<em>`: Emphasizes text. Similar to italics. Example: `<em>This content is emphasized.</em>`
- `<a>`: Anchor tag. Creates a link. The URL following href denotes where the link should travel to. Example: `<a href="http://www.epicodus.com">Epicodus</a>` - link to another web page
- `<img>`: Image tag. `<img src="img/kitten.jpeg" alt="A photo of a cute kitten.">` - link to an image located in img subdirectory, with alt text.
