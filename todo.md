# Todo

- Tokens
  - Color system (100-900)
    - [x] Base palette
    - [x] Automatic semantic token generation
  - Typography (100-900)
    - [x] Font families (base, heading, monospace)
    - [x] Font sizes (100-700, 600 being base normal size)
    - [x] Transform (bold, italics, etc)
  - Spacing (xs-xl)
    - [x] Spacing scale (margins, padding, etc)
    - [x] Basic block extend for universal padding (thanks bulma)
  - Misc (xs-xl)
    - [x] Border radius
    - [x] Transition durations
- Base Styles
  - [x] CSS Reset
  - [x] Default typography styles
  - [x] Link styles
  - [x] Selection styles
  - [x] Focus-visible defaults
- Layout system
  - Container
    - [x] Max widths
    - [x] Responsive padding
    - [x] Fluid container option
  - Grid
    - [ ] CSS grid abstraction
    - [ ] Responsive columns
    - [ ] Gap utilities
  - [ ] Flex utilities (direction, wrap, alignment, etc)
- Utility classes
  - [ ] Display (block, inline, inline-block, flex, grid, none)
  - [ ] Position (relative, absolute, fixed, sticky)
  - [ ] Overflow (hidden, auto, scroll)
  - [ ] Spacing (margin, padding, gap)
  - [ ] Text (align, weight, transform, truncate, wrap)
  - [x] Color (background, text, border)
  - [ ] Cursor (pointed, not-allowed, etc)
  - [ ] Width/Height (100%, auto, min/max variants, vh, etc)
  - [ ] Misc (z-index, shadows, transitions, etc etc)
- Components
  - https://www.w3.org/WAI/ARIA/apg/patterns/
  - https://open-ui.org/
  - [x] Forms (Input, textaera, select, checkbox, radio, label, field wrapper, help text, error message, and validation/disabled/focus states + size variants)
  - [x] Buttons (Solid, outline, ghost, link, and hover/active/disabled/loading states + size variants)
  - [x] Dropdown Select -- choices.js
  - [x] Chip
  - [x] Icons
  - [x] Sidebar
  - [x] Navbar
  - [x] Dropdown
  - [x] Menu
  - [x] Tooltips
  - [x] Card
  - [x] Modal
  - [x] Table
- [x] Everything built to be dark-mode first, with a light mode variant
- [x] Everything built with semantic HTML elements where possible, aria attributes where not, and using common design patterns over arbitrary class names
- [ ] Everything built to be customizable with utility classes to change colors, paddings, sizes, filled/unfilled, etc
- [x] Everything built to be generative, so I'm not manually creating new derived variables often
- [x] Everything built to be accessible by default

you already applied the style guide to the components, do it to the layouts and clean up choices/tabler/schemes/utilities before doing the following and then calling it good:

global is-element/top/etc system so that things like menus don't only have to be on element backgrounds.
global sizing system? is-xs, is-sm, etc?
global positional system? is-centered, is-end, is-aligned-end, etc?
blur navbar bg?
more usage of fluid-clamp, especially for positioning?
decouple tabler/choices / generate separate css files including them?
create more default schemes





-is-{color} variants of everything, including vivid/muted, especially for one-off elements. maybe make it a series of utility classes, but maybe not.
-is-size variants
-is-ghost / is-active / is-disabled variants
-is-loading variants
optional tokens for color (font, background, border, etc), size, font-size, visibility (including visibility at breakpoints) etc





cssisinuse:

Home > homepage for the site/docs, make it look good, provide links to view features/components/install

about > in a world filled with new and old css frameworks and front end tools, why make a new old-school one? explain all of the features that makes it unique (genetic tokens, )

Setup & Installation > explain that it's a css library that provides classes to help you style your html. you can use a precompiled css file or install the scss file to customize it. use a meta viewport tag to make it responsive. css & scss installation options. starter template html file

Kitchen Sink > quick display of every single element in every possible configuration, like a macy's showroom floor.


features and utilities are info
layouts are success
components are warning
css are danger


figure out line height cause im definitely doing it weirdly