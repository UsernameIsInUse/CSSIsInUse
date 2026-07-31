# Goal

The goal of CSSIsInUse is to create a semantic-first, utility-where-possible, generative (not AI), accessible framework with infinite themability.

## What does semantic-first mean?

Instead of every style being tied to a class, where possible styles will be applied to semantic HTML elements, aria attributes, and common design patterns instead of arbitrary class names. There will almost certainly still be arbitrary class names, we're just trying to avoid them.

## What does utility-where-possible mean?

Every element should be modifiable with common utility classes, including changing text, background, and border color, padding and margin sizes, outlined, filled, etc. Steal from tailwind, steal from bulma.

## What does generative (not AI) mean?

All colors, sizes, and variables will be generated from and reference only a few input variables. A base color for backgrounds and UI elements, primary color, info, warning, danger, success, padding and margin sizes, etc. Each of these will have variations automatically generated, and derived directly from the input variable. For example, changing the primary color css variable will change all derived elements as well.

## What does accessible mean?

If done right, contrast ratios should be more than met by default. The design pattern, as defined in above rules, should encourage semantic HTML and aria attributes.

## What does infinite themability mean?

Because of all of the above rules, generating themes should be simple and easy, from changing colors to fonts to sizes of things. You should only have to create a class setting a few variables, and all elements will be derived from that changing the entire look and feel of the site. Apply that to the html tag to change the look of the entire site, apply it to an element to change the look of that element and all child elements. Each theme should automatically include a dark and light mode, based on auto user preference or the data-theme attribute.

## Later Update

Turns out there's a reason why people generally don't make semantic-first frameworks. While this project certainly prefers if you use semantic elements and aria attributes, it does not require them because having asides and navs and articles mean different things based on context is more important than having no arbitrary classes. So, unfortunately, most things are arbitrary classes. What are you going to do. Oh well, there are some good utility classes with more to probably come, all colors and sizes and things are based on a few input variables, built-in themes are completely accessible, and it is infinitely themable.