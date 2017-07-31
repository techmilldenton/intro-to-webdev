---
layout: post
title: "Class vs ID Selectors"
tags:
date: 2017-07-30T18:50:34-05:00
---

Classes and ID's can both be used to select HTML elements on a page. However, the browser treats them slightly different when deciding which style rules to display.

The formula for this takes into account how many selector types, which looks like this:

> (inline styles, ID selector, class/pseudo-selector, element)

The browser simply calculates which selectors are used, and how many times, and from that determines the styles to apply.

See the [Further Reading](#further-reading) section for more.

# `.` vs `#`

- A particular `id` can only be attached to one element per web page, while the same `class` can be attached to many different elements on the same page.

- When referencing **classes** in CSS, use: `.`, for example:
```css
.intro {
  height: 100px;
  overflow: hidden;
}
```

- When references **ids** in CSS, use: `#`, example:
```css
#success--btn {
  color: rgb(20, 20, 20, .4);
  padding: 1em;
}
```

### Summary

The key take-away is that, in general, classes are a little easier to keep
track of and are more _general purpose_. Using an ID means that whatever
name you choose cannot be re-used. Also, let's say that you do decide to
use an ID to define some CSS properties. Whatever rules applied by the ID
will never get overridden by a style class - IDs are "_infinitely_" more
specific, so mixing the two is not recommended. In most cases, you can
avoid using an ID altogether.

# Further Reading

- [Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)
- [Understanding Style Precedence in CSS: Specificity, Inheritance, and the Cascade](http://vanseodesign.com/css/css-specificity-inheritance-cascaade/)
- [Specificity Calculator](https://specificity.keegan.st)
- [MDN/CSS/Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

