# 8fold Loom

The idea behind Loom is to make creating design systems easier, which may not necessarily make software development easier at first.

The following reflections are meant as personal perspectives and possible gaps or ways to "scratch our own itch" in the CSS design system space.

When describing pains and joys we will reference to example libraries and frameworks that appear to have the quality under examination. This reference is not meant as a positive or negative critique on the implementations as it is our view that if they did not deliver value to someone somewhere, they would not exist.

Finally while the assessment presents a dichotomy (pain vs. joy) it is meant as a tool to keep us from fence-sitting; the line is not hard and the scale is long.

We do not know if the world needs something different. With that said, 8fold may want something different.

## Joy

- Helpful, complete, and minimal documenation: TailwindCSS, Sass, 
- Utility classes for rapid development and styling before committing to a definition: TailWindCSS, USWDS,
- CSS-first philosophy: Sass
- Reduce duplication and file size for users - with minimal effort and scraping.
- Ability to write less raw CSS while receiving more at the end: Sass
- Accessibility as a primary concern when developing components: USWDS

## Pain

- The market in general seems kind of settled; many UI libraries that were "up and coming" now seem to have gone stail - if we don't want to use it, it's really not worth making a product out of it *and* depending on someone else to be around in the next 2 or 3 years is touch or go: Semantic UI, Scut, 
- Utility classes as anything beyond a means to a new means.
- Configuration (subtractive) over extension/convention (additive): TailWindCSS, BootStrap, Foundation
- Without customization sites risk looking and feeling the same; saw this particularly around 2015 as rapid prototyping was done a lot using Bootstrap, for example - not we may be experiencing a new problem as many seem to be open sourcing their design systems: Google Material Design, US Web Design System, 
- Pre-defined components, HTML structures, classes, IDs, and so on to accomplish its primary function: USWDS, Bootstrap

## Desired

- Helps in either teaching CSS practicess that help improve user and developer experience; with that priority order.
  - Style elements first.
  - Use attributes as selectors more than creating classes.
  - Classes are a last resort.
- Push new CSS features based on suporting browsers with 1.5% usage based on [CanIUse table](https://caniuse.com/usage-table), which means no support as of this writing for:
  - IE
  - Opera and Opera Mini
  - Android Browser
  - Opea Mobile
  - Firefox for Android
  - UC Browser for Android
  - QQ Browser
  - Baidu Browser
  - KaiOS Browser
- Favor progressive enhancement over graceful degradation or loss of functionality.
- Minimal dependencies; favor CSS + shorthands

## What can we use from CSS?

CSS offers various functions, making CSS more of a programming language not just a style definition language.

In short, everything but `attr()` without consideration.

|Yes |No |
|:--:|:--:|
| |attr()* |
|calc() | |
|cubic-bezier() | | 
|hsl() | |
|hsla() | |
|linear-gradient() | |
|repeating-linear-gradient() | | 
|radial-gradient() | |
|repeating-radial-gradient() | |
|rgb() | |
|rgba() | |
|var() | |

* can be used in specific use cases
