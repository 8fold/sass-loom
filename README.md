# 8fold Loom

An approach and toolset for weaving CSS.

## Installation

TBD 

This is a work in progress and, as with most of what we do, will probably only be turned into a library if:

1. it makes it easier for 8fold to use,
2. enough outside interest is expressed, or
3. both.

Given the bulk of this is an approach not a toolset though...you might already be "using" it. 😜 🖖

## Approach

### Values

- Vanilla CSS over libraries: Reduce barrier to entry and learning curve by staying close to CSS as defined by w3c recommendations.
- Progressive enhancement over graceful degredation: Design and development should be respectable regardless of technology used.
- Additive over subtractive: It's easier to add more of something than it is to take it away; let others season and spice their own food to their own tastes.

### Principles

- Catering to the most constrained includes the most people.
- The more pre- and post-processing is involved, the more complex the solution despite not needing to be in most cases.

### Practices

- Mobile-first: Defaults and target sizes are for the smallest screens with little bandwidth.
- CSS variables: We use CSS variables almost exclusively to give value to CSS properties.
- Extensible convenience: 

### Approach overview

Can be performed using CSS-only. 

A pre-processor like Sass can allow you to easily port an entire design system across multiple web properties without adding to the rendered CSS.

As a toolset, Loom proposes little-to-no opinions on the design system, HTML components, or technology stack; therefore, responsibility for accessibility and accommadation is left to the user.

With that said, examples use 8fold criteria for accessibility and accommadation, which is:

- over 90 percent of the design and interaction should available to
- browsers with a 1.5 usage rating according [Can I Use...](https://caniuse.com/usage-table). 

## Usage

The examples folder contains an iterative demonstration of this approach, include the original Sass file for generating the [8fold Handbook](https://handbook.8fold.link) site.

- [Example 2](https://github.com/8fold/sass-loom/blob/main/examples/sass_2.scss) demonstrates a CSS-only approach: Only CSS variables define property values. Reduces duplication, facilitates find-and-replace swapping, improved position to add themes without adding CSS. Main limitation to this approach we found to be in potential bloat when adding all variables from a design system.
- [Example 4](https://github.com/8fold/sass-loom/blob/main/examples/sass_4.scss) overcomes the limitation of the CSS-only approach by introducing Sass variables. Sass variables can be used to make an entire design system available while not adding anything to the CSS itself. CSS variables are then created as needed and reference the Sass variables. This establishes the main target CSS for all other approaches. Using the same overall design system across multiple sites becomes easier and depreacation become a matter of deleting the CSS variable without deleting the Sass variable. The limitation here is in readability.
- [Examples 5a](https://github.com/8fold/sass-loom/blob/main/examples/sass_5a.scss) to [5d](https://github.com/8fold/sass-loom/blob/main/examples/sass_5d.scss) overcomes this by using a Sass map and creating query and building functions to get to the values. The main limitation here comes in a degradation of readability.
- [Example 6](https://github.com/8fold/sass-loom/tree/main/examples/sass_6) overcomes this by creating a Sass module to house the Sass functions and mixins and then used by the main Sass file to generate the CSS.

...this work is ongoing as we expand from the 8fold Handbook. The hypothetical result is a library avaialble via NPM for use by ourselves, the work we do for practitioners, and possibly others.


## 8fold Loom considerations

The idea behind Loom is to make creating design systems easier, which may not necessarily make software development easier at first.

The following reflections are meant as personal perspectives and possible gaps or ways to "scratch our own itch" in the CSS design system space.

When describing pains and joys we will reference to example libraries and frameworks that appear to have the quality under examination. This reference is not meant as a positive or negative critique on the implementations as it is our view that if they did not deliver value to someone somewhere, they would not exist.

Finally while the assessment presents a dichotomy (pain vs. joy) it is meant as a tool to keep us from fence-sitting; the line is not hard and the scale is long.

We do not know if the world needs something different. With that said, 8fold may want something different.

This is the most raw section.

### Joy

- Helpful, complete, and minimal documenation: TailwindCSS, Sass, 
- Utility classes for rapid development and styling before committing to a definition: TailWindCSS, USWDS,
- Reduce duplication and file size for users - with minimal effort and scraping.
- Ability to write less raw CSS while receiving more at the end: Sass
- Accessibility as a primary concern when developing components: USWDS

### Pain

- The market in general seems kind of settled; many UI libraries that were "up and coming" now seem to have gone stail - if we don't want to use it, it's really not worth making a product out of it *and* depending on someone else to be around in the next 2 or 3 years is touch or go: Semantic UI, Scut, 
- Utility classes as anything beyond a means to a new means.
- Configuration (subtractive) over extension/convention (additive): TailWindCSS, BootStrap, Foundation
- Without customization sites risk looking and feeling the same; saw this particularly around 2015 as rapid prototyping was done a lot using Bootstrap, for example - not we may be experiencing a new problem as many seem to be open sourcing their design systems: Google Material Design, US Web Design System, 
- Pre-defined components, HTML structures, classes, IDs, and so on to accomplish its primary function: USWDS, Bootstrap
