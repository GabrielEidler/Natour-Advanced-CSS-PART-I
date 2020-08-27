
# Lectures Notes - by Gabriel Eidler

*template:*

**Lecture n**
- 

```


```


**Lecture I**
- The best way to perform a basic reset using the universal selector
- How to set project-wide font definitions
- How to clip parts of elements using clip-path

```
css architecture: always set up classes for your html file elements

typing css properties, you can write backimg and it will find background image for you ( AMAZING! )

CSS Shapes Resource: Clippy (url at jona's website)
```

**Lecture II**
- Easiest way to center anything with the *transform, top* and *left* properties

```
Block level elements goes the full width available, and it breaks the line after each element

Span is treated like a text, wo we need to change it's display type to block
```

**Lecture III**
- Cool CSS animations

```
There are 2 types of animations:

Using animation and @keyframes

or using the transition property

this is one of the most important properties in animation, and the different configurations will alter the "feel" in the user experience
animation-timing-function: ease-out;

in animation there is a shake bug, and the fix uses the *backFace-visibility* property

VS-CODE: ALT + CLICK => Multiple Cursors
```

**Lecture IV**
- What pseudo-elements and pseudo-classes are
- How and Why to use the ::after pseudo-element
- hover animation using the transition property


```
An inline element is treated like it's text, so you can influence it like you would a text element

The transition property needs to be specified in the initial state of the element

pseudo elements allow us to style certain parts of elements
    - For example the :after creates a virtual element right after the first one

You can use after to create an element that can stay behind the first one and add splash animations to it

example of a pseudo class:
    .btn-main:link{

    }
```

**Lecture V**
- 3 Pillars of writing good HTML and CSS

```
The three principles are:
    - Responsive Design
        works for all type of screen sizes and devices
            + Fluid Layouts
            + Media Queries
            + Responsive Images
            + Correct Units
            + Desktop-first Vs. Mobile-first Strategy
    - Maintainable and scalable code
        Write clean, understandable, scalable and reusable code
            + Clean
            + Easy-to-understand
            + Growth
            + Reusable
            + How to organize files
            + How to name classes
            + How to structure HTML
    - Web Performance
        make the website faster and smaller in size
            + Less HTTP requests
            + Less code
            + Compress code
            + Use a CSS preprocessor(like Sass)
            + Compress Images (Images are by far the biggest bottleneck in terms of website size)

```

**Lecture VI**
- How and why to use *rem*
- A great workflow for converting px to rem

```
    Rem is used because we will be able to change all the measurements in a page with one easy setting
        e.g. changing one global setting to convert the layout for a mobile frame
    
    The root font size is set with the html selector

    Having a rem = 62.5% (equals 10px), writing 10px is bad practice makes mental calculations a lot easier
```

**Lecture VII**
- The box model with box-sizing: border-box
- Inline, block-level and inline-block
- Stacking Contexts

```
With box-sizing: border-box, the padding is included in the total height and width (which honestly makes a lot more sense)

z-index are used for stacking context

Opacity different from one, a transform, a filter also creates a stacking context,
and because of that, even with the z index set, the stacking order doesn't work
as expected.
```

**Lecture VIII**
- The Think - Build - Architecture Mindset

```
Maintainable and scalable code => Clean, Modular, Reusable and Ready for Growth 

About Component Driven Design: “Simply put, component-driven development means designing your software applications 
by building loosely-coupled independent components.”        
                            - Saring, 2019

BEM Model for building meaningful class names:
    BEM stands for Block Element Modifier
        .block {}
        .block__element {}
        .block__element--modifier
    
    BLOCK: standalone component that is meaningful on its own
        e.g. class="btn" or class="recipe", these names can be reused all over the project
        one block can be nested in another
    
    ELEMENT: part of a block that has no standalone meaning 

    MODIFIER: a different version of a block or an element
        e.g. class="recipe__btn btn btn--round" or class="recipe__stat-name--1"

    Although is not the best way of formatting, BEM is a good standard to follow

The 7-1 Pattern
    7 different folders for partial Sass files,
        base/ - basic product definition
        components/ - one file for each component
        layout/ - overall layout of the project
        pages/ - styles for specific pages
        themes/ - in case there are different themes
        abstracts/ - code that doesn't output any css, such as variables
        vendors/ - all 3rd party css goes

    1 main Sass file to import all other files into a compiled CSS stylesheet
```

**Lecture IX**
- Introduction to Sass
- Compiling Sass with npm packages and scripts 

```
Sass is a CSS preprocessor, an extension of CSS that adds power and elegance to the basic language

Sass solves the CSS problem of being messy

Probably Styled components is the best option for React, but it's still useful to learn about Sass 

Sass syntax vs. SCSS syntax
    SCSS has indentations, which is better


```

**Lecture X**
-  Solution for floated child elements
-  Modifying child elements

```
Modifying child elements:
    .my-class:last-child{

    }

    .my-class:first-child {

    }

Sass, like Styled components, enables nesting

You shouldn't go deeper than 3 levels

when you float an element (right or left), the structure (child elements) collapses and
LOSES its Height! this is a common issue with floated elements

    Whenever you use float, you need to use the clearfix solution:

        1. Create a class called clearfix
        2. Put in these configurations:

            .clearfix::after {
                content: "";
                clear: both;
                display: table;
            }
Inline-block will create padding on top and bottom of text elements (reminder)

Using nesting, you can give different states config inside the main selector, as shown below:

    .btn-main {
        :link{
            //config 
        }

        :hover{
            //config 
        }
    }

```

**Lecture XI**
- Mixins, extends and functions

```
Mixin - Reusable variable with multiple lines of code
    for example, instead of copy/paste the .clearfix class, we use a mixin
    and add that mixin when I need to
        @mixin class-name{}

        and use it with:
        @include class-name;

    Mixin can accept variables as arguments (similar to a function)

Functions
    example: 
        @function($a, $b){
            @return $a / $b
        }

Extends - write a placeholder with different styles, and have a selector use that placeholder
    example:
        %btn-placeholder {
            //styles
        }
        usage:
        @extend %btn-placeholder;

    Extend is different from Mixin because it doesn't copy the styles into the selector, but rather copy the selector into the extend

    use Extend only for very related things!


```

**Lecture XII**
- converting project from CSS to SCSS

```
Valid CSS works in SCSS environment

```
