# Notes
## Basics
### Styling
```css
body {
  color: #FF0000;    /* Dark gray */
}
```
- CSS **rules** start with a **selector** that defines which [[HTML]] elements it applies to
- Then we declare **properties** like `color` and set their **values**
- Use `/* */` to denote comments
- To link a style sheet, inject the following code into the head of an html document:
```html
<head>
  <!-- Other header metadata -->
  <link rel="stylsheet" href="path-to-my-style.css"/>
</head>
```
- The value for a styles href can be absolute, relative, or root-relative.
- Many CSS properties require units of measurement for example:
```css
body {
  font-size: 18px;
}

h1 {
  font-size: 2em;
}
```
- The two most common are **px** and **em**
	- **px** refers to pixels.
	- **em** scales the current size of the property
	- For example if the font is 12px for body text `2em` would convert it to 24px.
```CSS
h1, h2, h3, h4, h5, h5 {
  font-family: "Helvetica", "Arial", sans-serif;
}
```
- You can chain selectors to change properties for many at once
- Some properties, like `font-family` accept multiple values. These properties try the value on the left and, if it fails, work their way to the value on the right.
```CSS
ul {
  list-style-type: circle;
}

ol {
  list-style-type: lower-roman;
}
```
- Each selector has many different properties. It's going to take a while to get used to all of them. 
- Some useful properties:
```css
a {
  text-decoration: none;
}

p {
  text-align: left;
}

h1, h2, h3, h4, h5, h6 {
  font-family: "Helvetica", "Arial", sans-serif;
  font-weight: normal;
}
```
- CSS is called cascading style sheets because styles can cascade from multiple places:
	1. Inline styles (don't do this)
	2. Page-specific styles
	3. External style sheets
	4. User-defined style sheets
	5. The browser's default style sheet
- Our `styles.css` file is an external style sheet
- Page-specific styles can be defined by inject a style tag into the head of a page:
```html
<head>
  <!-- Other header tags -->
  <style>
    body {
	  color: #0000FF;    /* Blue */
    }
  </style>
</head>
```
- Be warned: page specific styles are very difficult to maintain.
- Inline styles are just awfule:
```html
<p style='color: #990000; text-decoration: line-through;'>Some styled words</p>
```
- You can define multiple style sheets:
```html
<head>
  <link rel='stylesheet' href='styles.css'/>
  <link rel='stylesheet' href='product.css'/>
</head>
```
- When using multiple style sheets, order matters. Later links will override the styles from earlier ones.
### Layout
- Layout is edited by manipulating the [[CSS Box Model]]. Core components include:
	- Padding
	- Borders
	- Margins
	- Block boxes
	- Inline boxes
- HTML elements come in two flavors: block-level elements and inline elements.
```css
a {
  background-color: #B2D6FF;
  display: block;
}
```
- You can manipulate whether an element is block-level or inline with the display property. The above code is a simple button
- **Components of the CSS Box Model**:
	- Content - The text, image, or other media content in the element
	- Padding - The space between the box's content and its border
	- Border - The line between the box's padding and margin
	- Margin - The space between the box and surrounding boxes
- Each component can be adjusted:
```CSS
h1 {
  padding: 15px;
  border: 1px solid #5D6063;
  margin-bottom: 50px;
}

h2 {
  padding: 20px 10px;  /* Vertical Horizontal */
}

p {
  padding: 5px 10px 5px 10px; /* Top Right Bottom Left */
}
```
- CSS uses **vertical margin collapse** stacked blocks will not be separated by the combined distance of both margins but instead by the distance of the greatest margin.
- **Generic Boxes**. There are two types:
	- `<div>`
	- `<span>`
### CSS Selectors
```html
<p class='synopsis'>CSS selectors let you select HTML elements</p>
```

```css
.synopsis {
  color: #7E8184;    /* Light gray */
  font-style: italic;
}
```
- **Class Selectors**
	- Class selectors let you apply CSS styles to a specific css element.
	- They requre a `class` attribute on the HTML element in question
	- And a matching CSS class selector in the stylesheet
	- Note that class selectors are preceded by a dot
- **Container Divs**:
	- Divs can be used as containers to help layout the site.
- You can add multiple classes. For example:
```html
<div class='button synopsis'>Button</div>
```
- **Descendant Selectors**
	- You can chain classes and tags to get more specific for example:
```css
.synopsis em {
 font-style: normal;
}
```
- **Pseudo Classes for Links**
	- Links have a few basic pseudo classes:
		- `:link` - A link the user has never visited
		- `:visited` - A link the user has visited before
		- `:hover` - A link with the user's mouse over it
		- `:active` - A link that's being pressed down by a mouse (or finger)
	- For example:
```css
a:link {
  color: blue;
  text-decoration: none;
}

a:visited {
  color: purple;
}

a:hover {
  color: aqua;
  text-decoration: underline;
}

a:active {
  color: red;
}
```
- **ID Selectors**
	- You can only have one element with a specific ID per page
```html
<a id='button-2' href='nowhere.html'>Button</a>
```

```css
#button-2 {
  color: #5D6063;
}
```
- Use `#` to refer to id's in CSS
- Generally, just don't use id selectors
- **Except**... ID's can be used in URL fragments. For example:
```html
<!-- From the same page -->
<a href='#button-2'>Go to Button Two</a>

<!-- From a different page -->
<a href='selectors.html#button-2'>Go to Button Two</a>
```
- Holy cow! this is how sites do good footnotes!
## Flexbox
- Use `display: flex;` to create a flex container
- Use `justify-content` to define the horizontal alignment of items
- Use `align-items` to define the vertical alignment of items
- Use `flex-direction` if you need columns instead of rows
- Use the `row-reverse` or `column-reverse` values to flip item order
- Use `order` to customize the order of individual elements
- Use `align-self` to vertically align individual items
- Use `flex` to create flexible boxes that can stretch and shrink
## Starter Properties
- `color` - Sets an elements text color
- `background-color` - Sets the background color of an element
- `font-family` - Sets the font family
	- Can be a comma separated list of families to use in decreasing order
- `font-size` - Sets the font size. Uses `em` or `px`
- `font-weight` - Affects the boldness of the text
- `text-align` - Aligns text horizontally within an element
- Image `height` and `width` - Set the height and width of an image
	- By default, setting one to a size and the other to auto will retain the images proportions