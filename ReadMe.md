
# Lectures Notes - by Gabriel Eidler

*template:*

**Lecture X**
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

Sudo elements allow us to style certain parts of elements
    - For example the :after creates a virtual element right after the first one

You can use after to create an element that can stay behind the first one and add splash animations to it
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
            + Compress Images (This is by far the biggest bottleneck in terms of website size)

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