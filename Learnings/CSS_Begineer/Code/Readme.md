What is CSS?
------------
1. CSS stands for Cascading Style Sheets. 
2. CSS is the language we use to style an HTML document.
3. CSS describes how HTML elements should be displayed.
4. CSS saves a lot of work. It can control the layout of multiple web pages all at once.
5. External stylesheets are stored in CSS files.

### Why use CSS?
CSS is used to define styles for our web pages, including the design, layout and variations in display for different devices and screen sizes.

## CSS solved a big problem:
1. HTML was never intended to contain tags for formatting a web page!
2. HTML was created to describe the content of a web page.
3. When tags like<font>, and color attributes are added to HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process.
4. To solve this problem, the World Wide Web Consortimum(W3C) created CSS.
5. CSS removed the style formatting from the HTML page.

### CSS Syntax:
* A CSS rule consists of a selector and a declaration block.
example: h1 {color:blue; font-size:12px;}
Here:
h1 -> selector, 
elements inside {} -> Declaration

* The selector point to the HTML element we want to style.
* The declaration block contains one or more declarations seperated by semicolons.
* Each declaration includes a CSS property name and a value, seperated by a colon.
* Multiple CSS declarations are seperated with sumicolons, and declaration blocks are surronded by curly braces.

## Paragraph (<p> element) Example:

p {
  color: red;
  text-align: center;
}
* Here, p is a selector in CSS. It points to the HTML element we want to style: <p>.
* color is a property, and red is the property value.
* text-align is a property, and center is a property value.

## CSS Selectors:

* CSS selectors are used to "find/select" the HTML elements we want to style.
* We can divide CSS selectors into five categories. They are: 
1. Simple selectors: select elements based on name, id, class.
2. Combinator selectors: select elements based on a specific relationship between them.
3. Pseudo-class selectors: select elements based on a certain state.
4. Pseudo-elements selectors: select and style a part of an element.
5. Attribute selectors: select elements based on an attribute or attribute value.

## CSS Id Selector:
* An id name can not start with a number.

## CSS Class Selector:
* A class name can not start with a number.

## All CSS Simple Selectors:
Selector | Example | Example description
-------- | ------- | -------------------
#id | #firstname | Selects the element with id="firstname"
.class | .intro | Selects all elements with class = "intro"
element.class | p.intro | Selects only <p> elements with class "intro"
* | * | Selects all elements
element | p | Selects all <p> elements
element, element, ... | div, p | Selects all <div> elements and all <p> elements 