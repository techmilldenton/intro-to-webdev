---
layout: post
title: "Media Queries and Resonsive Design"
tags:
date: 2017-07-30T19:16:46-05:00
---

Media queries will allow you to add support for multiple viewport sizes by
splitting style properties into separate rules based on things like screen
width or height. For more and to see a comprehensive list, see [Further Reading](#further-reading).

- [Lesson - Intro to Programming (Evening)  Git, HTML & CSS Media Queries and Responsive Design](https://www.learnhowtoprogram.com/intro-to-programming-evening/git-html-css-de7fdaad-6b62-4319-ada7-ce4db6d0ef86/media-queries-and-responsive-design)

# Terminology

- **Media query**: A block of CSS applied only when certain conditions about the size or type of screen/window a user is viewing our content with are true. (ie: CSS associated with a media query with a max-width of 500px would only apply its styles when the viewport width is below 500px).

- **Breakpoint**: The point at which a media query's condition becomes true. A media query with a max-width of 500px will apply its styles when the viewport is less than 500px. 500px is then the break point.

- **Viewport**: The tool a user is viewing content with. Usually a browser window on a computer, phone, or tablet.

- **Responsive web design**: An approach to web design focused around providing the best viewing and navigation experience for the specific device and screen size a user is viewing content with.

- **Media types**: The type of media device the user is viewing content with (such as print, screen, handheld, or all)

- **Media features**: Specific properties about the manner the user is viewing content; including width and height of viewport, orientation of device, etc.

Examples
The following query will make the background red and text white when the browser window has a width below 768px:
```css
@media screen and (max-width:  768px)  {
    body {
        background:  #FF6347;
        color: #FFF;
    }
}
```
In the code above:

- `screen` is the **media type**.
- `768px` is the **breakpoint**.
- `max-width` is a **media feature**.
- `body` is a **selector**.
- `background` and `color` are **properties**.
- `#FF6347` and `#FFF` are **values**.

# Additional Resources
- MDN - [Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
- MDN - [@media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)
- Example usages of media queries - [Mediaquer.ies](http://mediaqueri.es/)

# Further Reading

- [Responsive Web Design Basics](https://developers.google.com/web/fundamentals/design-and-ui/responsive/)
- [Media Queries for Standard Devices](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)
- [Logic in Media Queries](https://css-tricks.com/logic-in-media-queries/)
- [How To Use CSS3 Media Queries To Create a Mobile Version of Your Website (from 2010)](https://www.smashingmagazine.com/2010/07/how-to-use-css3-media-queries-to-create-a-mobile-version-of-your-website/)
