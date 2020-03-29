# Notes for CSS
## Box Model
- Content
- Border
- Padding
- Margin

## Display
types:
- block
- inline
- inline-block
- none

### block
- take the whole line width
- **can spicify the width in CSS**
- **do NOT allow other elements on the same line**
- e.g.
  - `<h1> ... <h6>`
  - `<p>`
  - `<div>`
  - `<form>`
  - `<ul>, <ol>, <li>`
### inline
- only take the necessary width
- **cannot spicify the width in CSS**
- **allow other elements on the same line**
- e.g
  - `<span>`
  - `<img>`
  - `<a>`
### inline-block
- **can spicify the width in CSS**
- **also allow other elements on the same line**
### none
- hide the element as if the element is removed
- (`visibility: hidden` is different, it hides the content but keep the position and size)

## Positioning
types:
- static
- relative
- absolute
- fixed

### static
- HTML default positioning

### relative
- relative to the default (**static**)positioning 
- coordinates properties:
  - top
  - right
  - bottom
  - left
- move away from the defalt position as the coordinates specified
- This is like giving margins on top, right, bottom, left from its default position
- **relative positioned element does NOT affect other elements' positions**

### absolute
- relative to the closest parent that is positioned relatively (most common one is the `<body>` element)
- coordinates properties:
  - top
  - right
  - bottom
  - left
- the coordinates properties specify the distances from the parent element on top, right, bottom, left
- **absolute positioned element will affect other elements' positions, as if this element is taken away from the original positioning flow**

### fixed
- similar to absolute
- but fixed position when scolling 

## Centering
- centering text
  - `text-align: center`
- centering an element that has a width
  - `margin: 0 auto;`
  - **inline elements do NOT have a width, so cannot use this**

## Font Family
- types:
  - serif
  - sans-serif
  - monospace

## Font size
- static
  - `font-size: 16px;`
- dynamic
  - `font-size: 120%`
  - `font-size: 1.2em`
  - by default, 100% = 1em = 16px
  - **BUT percentage and em are relative to the parent's font size setting, they will inherit from parent's font size as the base**
  - `font-size: 1.2rem`
  - rem is relative to the root font size, it will not inherit parent's font size.
  - **1rem = 16px**

## Float
- float
  - make an element float to left or right, allow text to wrap around it
  - `float: left`
  - `float: right`
- clear
  - used on text to stop wrapping around other element
  - `clear: left`
  - `clear: right`
- **ONLY use float to wrap text around an element (e.g. image), do NOT use float to position elements**


## z-index
- stacking order on z-axis by default
  - the HTML element below is on top
  - the child element is on top of parent element
  - positioned element (i.e. position is not static) is on top of static positioned element
  - CSS z-index property:
    - by default `z-index: 0`
    - larger `z-index` is on top, e.g. `z-index: 1`
    - can be negative, `z-index: -1`
    - **Noted that only when two elements are both positioned, the order will be determined by comparing z-index values**

## Media Query
- format: `@media <media types> <media features> { CSS Styles }`
  - media types (optional)
    - all
    - print (printer)
    - screen
    - speech (screen reader)
  - conditions:
    - `min-width: 500px` (when width is larger than or equal to 500px)
    - `max-width: 1000px` (when width is less than or equal to 1000px)
  - logical operators:
    - and
    - not
    - only

## Code Refactoring
    - Readability
    - Modularity
    - Efficiency
    - Length