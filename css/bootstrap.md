# Notes for Bootstrap
## Bootstrap uses
- Responsive
  - responds to the viewport
- Pre-styled elements

## Layout

### Container
- class `container` sets a `max-width` at each responsive breakpoint
- class `container-fluid` is full width, no margin `width: 100%`at all breakpoints

### Grid System
- each row can be divided into 12 units
- different screen size:
  - extra small
  - small (sm) (mobile phones)
  - medium (md) (tablets)
  - large (lg) (laptops)
  - extra large (xl) (large desktops)
- inside a row div `<div class="row"> </div>`
- column class examples:
  - col-xl-2 (takes 2 units when size is extra large)
  - col-lg-3 (takes 3 units when size is large or more)
  - col-md-4 (takes 4 units when size is medium or more)
  - col-sm-6 (take 6 units when size is small or more)
  - col-12 (take 12 units when size is extra small or more)
- larger column classes will overwrite smaller column classes (e.g. col-xl-2 overwrites col-lg-3 when it's extra large size)
- when smaller size is not specified, by default it takes 12 units

## Components

### Button
- example:
  - dark color, large size
  - `<button type="button" class="btn btn-dark btn-lg btn-block"> click me </button>`

### Nav-bar
- classes:
  - ul `navbar-nav`
    - li `nav-item`
    - a `nav-link`
  - `navbar-brand`
  - collapse contents: `collapse navbar-collapse`
  - collapse button: `navbar-toggler`

### Carousel
- A slideshow component for cycling through elements—images or slides of text
- classes:
  - `carousel`
  - etc.


