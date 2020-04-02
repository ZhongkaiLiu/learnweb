# Notes for jQuery

## include jQuery and JS in HTML
- include jQuery script and other JS codes at the end of the HTML document, to make sure that HTML elements already exist when running JS codes
- jQuery liberary should be above other JS codes

## jQuery Selector
- `jQuery(<CSS Selector>)`, similar to `document.querySelectorAll(<CSS Selector>)`
- `$()` is the shorthand for `jQuery()`, which is usually used
- `$("button")` returns all button elements
- **Note that `$()` will return all elements that match, and methods applied to this selector will also be applied to all elements that match**

## Manipulating styles in jQuery
## Directly
- get CSS styles
  - `$("h1").css("color")`
- set CSS styles
  - `$("h1").css("font-size", 32px)`
## Using classes
- add classes
  - `$("h1").addClass("class1 class2 ...")`
- remove classes
  - `$("h1").removeClass("class1 class2 ...")`
- toggle classes
  - `$("h1").toggleClass("class1 class2 ...")`
- check whether an element has a class
  - `$("h1").hasClass("class1")`, return boolean

## Manipulating text in jQuery
- get text
  - `$("h1").text()`
- set text
  - `$("h1").text("change text to this")`
- get HTML
  - `$("h1").html()`
- set HTML
  - `$(h1).html("<strong>new content</strong>")`

## Manipulating attributes in jQuery
- get attribute values
  - `$("img").attr("src")`
  - `$("h1").attr("class")`
- set attributes
  - `$("a").attr("href", "www.google.com")`

## Event listener in jQuery
- click event
  - `$("h1").click( function() {...} )`
- keydown event
  - `$(document).keydown( function(event) {...} )`
  - select the whole document `$(document)`
- general way to add event listener
  - `$("button").on(<event type>, function(event) {} )`

## Add and remove HTML elements
- add before
  - `$("h1").before(<div>new content</div>)`
- add after
  - `$("h1").after(<div>new content</div>)`
- add inside at the beginning
  - `$("h1").prepend(<div>new content</div>)`
- add inside at the end
  - `$("h1").append(<div>new content</div>)`
- remove
  - `$("h1").remove()`

## Animations in jQuery
- hide, show and toggle
  - `$("h1").hide()`
  - `$("h1").show()`
  - `$("h1").toggle()`
- slide up and slide down
  - `$("h1").slideUp()`
  - `$("h1").slideDown()`
  - `$("h1").slideToggle()`
- fade out and in
  - `$("h1").fadeOut()`
  - `$("h1").fadeIn()`

## loop through elements
- use `.each()` method
  - `$("button").each(function() {...})`
- use `$(this)` to select current element inside the callback function