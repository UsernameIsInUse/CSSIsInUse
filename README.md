# CSSIsInUse

Like a lot of hobbiest web devs, front end isn't my specialty. I like working with Flask to create the functionality of what I'm after, and would often just write a really long, really messy CSS file by hand to apply styles. Clunky, messy, arbitrary / random class names, z-index problems all over the place. But, I would make it work, and it would have all of the functionality I wanted and needed.

In trying to become a better front end dev, I wanted something that maybe looked a little more professional and designed, so I turned to various CSS frameworks. The problem was, they all somehow felt even clunkier to use than my bespoke solutions, were built from practices I just absolutely don't jive with (being forced to use Tailwind would be the death of me), and none of them had some specific, and what I thought would be very popular features that I wanted.

So, while trying to retrofit Bulma into what I wanted, I learned SCSS, and decided to give making my own a crack.

## What's different?

The goal of CSSIsInUse is to create a semantic-where-possible, monogenetic, accessible-by-default framework with infinite themability.

## What does semantic-where-possible mean?

A common issue with CSS frameworks is that the class names are completely arbitrary. Why is a card called a card when it's just another div? Why does everyone just use divs for everything and apply the right class when there are semantic elements that could be used?

Well, the problem is that semantic elements often can be used in lots of situations. Applying styles to an html element and expecting it to always be seen in a specific way every time it's used is not really practical. So, unless you're making something really simple, a complex CSS framework can't be semantic-first. So, instead, this is semantic-where-possible. If you use an h1 tag, it'll always display the same everywhere. You want it to be smaller? Just use a smaller header. Yes, buttons can be anchor tags or buttons, so we'll use `.button`. But if you put a table somewhere and don't expect it to be styled like a table, I think you're using tables wrong. We're just going to style all tables like they're tables. This isn't the early 2000's, we have flexbox and grid for site-wide structure.

The "kitchen sink" I've provided should be using semantic HTML elements in all applicable places, as well as aria attributes and common design patterns, but we can't force that without limiting design possibilities, so semantic-where-possible it is.

## What does monogenetic mean?

Everything in CSSIsInUse, including all colors, sizes, paddings, corner-roundnesses; all variables are derived from a few common ancestor variables you set up right at the start. Default padding is 1rem, which them determines the small padding and large padding, which multiply it by various numbers. There are a few defined "breakpoints" which determine the sizing of sections, containers, columns, etc. Colors are defined in a file, split up into OKLCH colors, which are used to generate all of the colors for the entire site, including backgrounds, texts, elements, in dark and light mode.

## What does accessible-by-default mean?

By default, if you just plug in CSSIsInUse, contrast ratios should be more than met by default. If you follow the structure of the kitchen sink, it should encourage correct usage of semantic HTML and aria attributes.

## What does infinite themability mean?

This is the biggest differentiator between CSSIsInUse and other frameworks. Because of all of the above rules, creating themes are simple and easy. You only have to create a class/data-scheme setting a few variables, register it in the color system, and all elements will be derived from that changing the entire look and feel of the site. Apply that to the body tag to change the look of the entire site, apply it to an element to change the look of that element and all child elements. Each theme automatically includes a dark and light mode, based on auto user preference or the data-theme attribute.

## ...So?

So, because of all of that, we have a framework that takes care of light/dark mode for you, lets you paint it however you want (including having dozens of themes that users can apply, or a different theme per section, or whatever), doesn't really care about "breakpoints" in the same way that Bulma or other frameworks do and just handles mobile mostly for you, and is super easy to customize and override with just a few CSS variables on top of everything rather than having to untangle a long and complicated SCSS web. The SCSS part is mostly just to separate concerns into different files, and allow quick generation of classes and variables through functions.
