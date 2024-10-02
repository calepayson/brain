# Basic HTML

## Boilerplate

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
</body>
</html>
```

## Common Tags and Elements

### Text Formatting

- **Headings**
	- `<h1></h1>` - Heading one
	- `<h2></h2>` - Heading two
	- `<h3></h3>` - Heading three
	- `<h4></h4>` - Heading four
	- `<h5></h5>` - Heading five
	-  `<h6></h6>` - heading six
- **Paragraph**
	- `<p></p>` - Denotes a paragraph
- **Line Break**
	- `<br>` - Equivalent to `\n`
- **Horizontal Rule**
	- `<hr>` - Draws a line across the page
- **Text Styles**
	- `<strong></strong>` or `<b></b>` - Bold text
	- `<i></i>` or `<em></em>` - Italic text
	- `<u></u>` - Underlined text
	- `<sup></sup>` - Superscript
	- `<sub></sub>` - Subscript

### Links and Images

- **Hyperlink**
	- `<a href="https://www.example.com"></a>` - Links to `example.com
- **Email Link**
	- `<a href="mailto:someone@example.com"></a>` - Sends and email to `someone@example.com`
- **Image**
	- `<img src="image.jpg" alt="Description of image>` - Displays `image.jpg`. Displays alt text if the image can't be found

### Lists
\
- **Unordered List**
	- `<ul><li></li></ul>` - Displays an unordered list of list items.
- **Ordered List**
	- `<ol><li></li></ol>` - Displays an ordered list of list items.
- **Definition List**
	- `<dl><dt></dt><dd></dd></dl>` - Displays a list of terms and definitions

### Tables

- **Basic Table Structure**
```html
<table>
  <tr>
    <th></th>
    <th></th>
  </tr>
  <tr>
	<td></td>
	<td></td>
  </tr>
</table>
```

### Forms

- **Form Element**
	- `<form action="submit-form.php" method="post"></form>` - Defines a form that submits to `submit-form.php` with a `post` method
- **Input Types**
	- `<input type="text" name="username">` - Defines a text input with the name `username`
	- `<input type="password" name="password">` - Defines a password input with the name `password`
	- `<input type="submit" value="Submit">` - Defines a submit input with the value `Submit`
	- `<input type="reset" value="Reset">` - Define a reset input with the value `Reset`
- **Checkbox and Radio**
	- `<input type="checkbox" name="option1" value="A"></br>` - Define a checkbox input with the name `option1` and a value of A. You can use text between the `<input>` and `</br>` elements
	- `<input type="radio" name="choice" value="X"></br>` - Define a checkbox input with the name `choice` and a value of X. You can use text between the `<input>` and `</br>` elements
- **Textarea**
	- `<textarea name="message" rows="5" cols="30"></textarea>` - Define a text area of the given size
- **Select Dropdown**
```html
<select name="options">
  <option value="value1"></option>
  <option vlaue="value2"></option>
</select>
```

### Semantic Elements (HTML5)

- **Layout Elements**
	- `<header></header>` - Define a header
	- `<nav></nav>` - Define navigation links
	- `<section></section>` - Define a logical section
	- `<article></article>` - Define the content of an article
	- `<aside></aside>` - Define a sidebar
	- `<footer></footer>` - Define a footer

### Media

- **Audio**
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio
```
- **Video**
```html
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

### Embedded Content

- **Iframe**
```html
<iframe src="https://www.example.com" width="600" height="400"></iframe>
```

## Global Attributes

These attributes can be used with any HTML element.
- `id` - Unique identifier for the element
- `class` - CSS class for styling
- `style` - Inline CSS styles
- `title` - Extra information about the element (displayed as a tooltip)
- `lang` - Language of the elements content.
- `dir` - Text direction (`ltr`, `rtl`)

## Comments

```html
<!-- This is a comment -->
```

## Character Entities

Use character entities to display reserved characters
- `&lt;` - `<`
- `&gt;` - `>`
- `&amp;` - `&`
- `&quot;` - `"`
- `&apos;` - `'`
- `&nbsp;` - Non-breaking space

## Met Tags

- **Character Set**
```html
<meta charset="UTF-8">
```

- **Viewport for Responsive Design**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- **Page Description and Keywords**
```html
<meta name="description" content="Page descritpion here">
<meta name="keywords" content="HTML, CSS, XML, JavaScript">
```

## Linking [[CSS]] and [[JavaScript]]

- **External CSS**
```html
<link rel="stylesheet" href="styles.css">
```

- **Internal CSS**
```html
<style>
  /* CSS code here */
</style>
```

- **External JavaScript**
```html
<script src="script.js"></script>
```

- **Inline JavaScript**
```html
<script>
  // JavaScript code here
</script>
```

## Special Input Types (HTML5)

- **Email and URL**
```html
<input type="email" name="email">
<input type="url" name="website">
```

- **Number, Range, Date, Time**
```html
<input type="number" name="quantity" min="1" max="10">
<input type="range" name="points" min="0" max="100">
<input type="date" name="bday">
<input type="time" name="appt">
```

- **Color Picker**
```html
<input type="color" name="favcolor">
```

## Block vs Inline Elements

- **Block-level elements** start on a new line and take up the full width available
	- Examples: `<div>`, `<h1>` to `<h6>`, `<p>`, `<form>`, `<header>`, `<footer>`
- **Inline elements** do not start on a new line and only take up as much width as necessary
	- Examples: `<span>`, `<a>`, `<img>`, `<strong>`, `<em>`

## Accessibility and SEO Tips

- Use `alt` attributes for images
```html
<img src="image.jpg" alt="Description of image">
```

- Use **semantic tags** to improve readability
```html
<nav>...</nav>
<main>...</main>
<article>...</article>
```

- Use **heading tags** in order
```html
<h1>Main Title</h1>
<h2>Subheading</h2>
```
# Notes
- Use `<a target="_blank">Content</a>` to launch links in new tabs or windows.
- Use `<a rel="noopener noreferrer">` for best security practices
- There are two kinds of links:
	- **Absolute Links** - link to other web pages
	- **Relative Links** - link to our own web page
- index.html should exist at the root directory
- All other pages should be under a `pages/` directory
## Elements and tags
- Elements are containers for content.
- Tags specify the form of that content.
- Elements usually consist of opening and closing tags.
## Boilerplate
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
  <body>
  </body>
</html>
```
