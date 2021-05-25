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

### Three Ways to Insert CSS:
There are three ways of inserting a style sheet:
* External CSS
* Internal CSS
* Inline CSS

### External CSS:
* With an external style sheet, we can change the look of an entire website by changing just one file!
* Each HTML page must include a reference to the external style sheet file inside the `<link>` element, inside the head section.
* An external style sheet can be written in any text editor, and must be saved with .css extension.
* The external .css file should not contain any HTML tags.
* >Warning: We don't need to add a space between the property value and the unit (such as `margin-left: 20 px;`).
The correct way is: `margin-left:20px;`
* Example
```
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
```

### Internal CSS:
* An internal style sheet may be used if one single HTML page has a unique style.
* The internal style is defined inside the `<style>` element, inside the head section.
* Example: `mystyle.css` is an external css file.
```<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
```

### Inline CSS:
* An inline style may be used to apply a unique style for a single element.
* To use inline styles, add the `style` attribute to the relevant element. The `style` attribute can contain any CSS property.
* An inline style loses many of the advantages of a style sheet (by mixing content with presentation). We should use this method sparingly.
* Example:
```
<body>
<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
</body>
```

### Multiple Style Sheets:
* **If some properties have been defined for the same selector (element) in different style sheets, the value from the last read style sheet will be used.**
* Example:
1. We assume that and external style sheet has the following style for `<h1>` element
```
h1 {
  color: navy;
}
```
2. Then we assume that an internal style sheet also has the following style for the `<h1>` element:
```
h1 {
  color: orange;
}
```

3. If the internal style is defined after the link to the external style sheet, the `<h1>` elements will be "orange":
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
<style>
h1 {
  color: orange;
}
</style>
</head>
```

4. If the internal style is defined before the link to the external style sheet, the `<h1>` elements will be "navy":
```
<head>
<style>
h1 {
  color: orange;
}
</style>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
### Cascading Order:
1. Inline style.
2. External and Internal style sheets.
3. Browser default.

### CSS Comments:
* CSS comments are not displayed in the browser, but they can help document our source code.
* Comments are used to explain the code, and may help when we edit the source code at a later date.
* Commnets are ignored by browsers.
* A CSS comment is placed inside the `<style>` element, and starts with `/*` and ends with `*/`

### CSS Colors:
Colors are specified using predefined color names, or RGB, HEX, HSL, RGBA, HSLA values.

### RGB Value:
* In CSS, a color can be specified as an RGB value, using this formula:
rgb(red, green, blue)
  * Each parameter defines the intensity of the color between 0 and 255.
  * For example, 
    * `rgb(255, 0, 0)` is displayed as red, because red is set to its highest value(255), and the others are set to 0.
    * To display black, we set all color parameters to 0, like this: `rgb(0, 0, 0)`.
    * To display white, we set all color parameters to 255, like this: `rgb(255, 255, 255)`.
    * Shades of gray are often defined using equal values for all the 3 light sources.
  
  
