# Notes for JavaScript DOM

## JavaScript 
- Methods
  - inline
  - `<h1 onload="console.log('hello')"></h1>`
  - internal
  - `<script>// JS codes here</script>`
  - external
  - `<script src="code.js"></script>`
- Position to place JS is important
  - usually place JS codes at the end of `<body>` element
  - if JS codes is at the beginning of HTML file, it may fail to get the HTML elements, because they may not exist yet.

## Document Object Model (DOM)
JS view the HTML file in a hirachical way
- document
  - html
    - head
      - meta
      - title
      - ...
    - body
      - h1
      - p
      - ...

## JS Object
- objects have properties and methods
- DOM objects gotten from HTML file also have properties and methods
  - e.g. `button`
    - properties:
      - `innerHTML`
      - `style`
      - `firstChild`
    - methods:
      - `click()`
      - `appendChild()`
      - `setAttribute()`
- get properties:
  - `button.innerHTML`
- set properties:
  - `button.innerHTML = "something here"`

## JS DOM Selectors
### get elements
- tag name
  - `document.getElementsByTagName("h1")`
  - return an array of objects
- class name
  - `document.getElementsByClassName("class1")`
  - return an array of objects
- id
  - `document.getElementById("id1")`
  - return only one object
### Query Selectors
- `document.querySelector("<selector>")`
  - `<selector>` can be anything like CSS selector
    - e.g.
      - `HTML tag`
      - `class`
      - `id`
      - combined selectors (`li ul`, `h1#title`, etc.)
  - only return the first object that matches the selectors
- `document.querySelectorAll("<selector>")`
  - return an array of all objects that match the selectors


## DOM Manipulating
### Change CSS Styles
- `document.querySelector("h1").style.fontSize("10rem");`
- differences:
  - JS use camel case:
    - `fontSize` instead of `font-size`
  - specify style by a string
    - `"10rem"`

### Separation of concerns
- using JS to change styles directly is NOT good
- separation of concerns:
  - HTML: structure
  - CSS: styles
  - JS: behaviour
- when JS needs to change styles, add, remove, toggle classes to the HTML element
  - use `classList` property to get and set class
  - `document.querySelector("h1").classList.add("new-class")`
  - `document.querySelector("h1").classList.remove("old-class")`
  - `document.querySelector("h1").classList.toggle("class-name")`
  - toggle means add the class if there's no class, remove the class if the class already exist

### Get and change content
- get and change content inside contain HTML element
  - `document.querySelector("h1").innerHTML`
  - `document.querySelector("h1").innerHTML = "<strong>some text</strong>"`
  - **Note that this may also return HTML codes, and we can also give HTML codes**
- get and change text content
  - `document.querySelector("h1").textContent`
  - `document.querySelector("h1").textContent = "text"`

### Get and change HTML element attributes
- view attributes:
  - `document.querySelector("a").attributes;`
- get the value of attribute:
  - `document.querySelector("a").getAttribute("href");`
- set the value of attribute:
  - `document.querySelector("a").setAttribute("href", "https://www.google.com");`


## Event listener
- add event listener to a HTML element
  - `element.addEventListener(<event type>, <handler function>)`
  - `document.querySelector("button").addEventListener("click", eventHandler)`
- can also add event listener to the whole document
- the anonymous function can also take the **event** as argument input
- `document.addEventListener("keydown", function(event) {...} )`