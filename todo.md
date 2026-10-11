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
global sizing system? is-xs, is-small, etc?
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

Top of the pyramid are utilities, which are the class versions of the tools and tokens that are built into every component. Utilities include standalone utilities like block, pre, radius changes, font size changes, etc, as well as component-specific utilities to change color, sizing, etc. This is the most granular detail work you can do, modifying how an individual element or component looks.

Next are components, which are individual elements as well as groups of elements which use classes to create a design. This includes simple single-element classes like chips, buttons, inputs, cards, etc, but also more complex structures with multiple elements needed to make them function correctly, like menus, modals, navbars, dropdowns, etc. These are designed using tokens and tools in a specific way, but can be overridden using global or component-specific utilities.

Next is layout, which are a components that are designed specifically to structure a page rather than be content in of itself. They are functionally identical to components in that they can be one-or-multiple elements, are designed using tokens and tools, and can be overridden using global or component-specific utilities. They include sections, containers, columns, main and sidebar, and the navbar.

Next are tools, which are mixins and functions used to create components, layouts, and utilities. These functions and mixins allow for things like transitions, glows, focus, whether something is scrollable, the fluid clamp system to remove the need for breakpoint media queries, etc. 

Finally there are tokens, which is the basis for the look of the entire site. These include the generated color tokens created by schemes, as well as the specified tokens in base. These control the look and feel of everything, including text and icon sizes, line heights, container widths, paddings/margins, sidebar and navbar sizes, font weights, border radii, opacities, glows, blurs, fonts, integration overrides, z-index, and color schemes. These can be edited directly or during runtime to increase padding, change colors, etc -- and because every element and component is built using them, changing one token can change every component at once. Tokens are also designed to be genetic, often referencing each other using calc to create new sizing variations, so often just changing the base version of a token will change all tokens in that category, such as padding.


Accordion

cssisinuse:

Home > homepage for the site/docs, make it look good, provide links to view features/components/install

about > in a world filled with new and old css frameworks and front end tools, why make a new old-school one? explain all of the features that makes it unique (genetic tokens, )

Setup & Installation > explain that it's a css library that provides classes to help you style your html. you can use a precompiled css file or install the scss file to customize it. use a meta viewport tag to make it responsive. css & scss installation options. starter template html file



on mobile, close sidebar on item click