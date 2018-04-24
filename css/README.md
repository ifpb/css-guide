# CSS

* [Problem](#problem)
* [How to apply your CSS to your HTML](#how-to-apply-your-css-to-your-html)
  * [Inline styles](#inline-styles)
  * [Internal stylesheet](#internal-stylesheet)
  * [External stylesheet](#external-stylesheet)
  * [Mixed stylesheet](#mixed-stylesheet)
* Syntax
  * [Properties](#properties)
  * [Selectors](#selectors)
  * [Functions](#functions)
  * [At-rules](#at-rules)
  * [Media Queries](#media-queries)
  * [Comments](#comments)
* [Inheritance](#inheritance)
* [References](#References)

## Problem
---

### First Web site to Zen Garden

* [Browse the first website using the line-mode browser simulator](http://line-mode.cern.ch/www/hypertext/WWW/TheProject.html)
* Zen Garden (style: [1](http://www.csszengarden.com), [2](http://www.csszengarden.com/221/), [3](http://www.csszengarden.com/220/))

### [Obsolete and deprecated elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Obsolete_and_deprecated_elements)

#### [`<center>`: The Centered Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center)

```html
<center>
  <p>Lorem ipsum dolor</p>
</center>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <center><p>Lorem ipsum dolor</p></center>
</div>

#### [`<big>`: The Bigger Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/big)

```html
<p>Lorem ipsum dolor sit amet, <big>consectetur adipisicing elit.</big></p>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p>Lorem ipsum dolor sit amet, <big>consectetur adipisicing elit.</big></p>
</div>

#### [`<font>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/font)

```html
<font size="20px" color="red" face="Helvetica">Lorem ipsum dolor</font>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
<font size="20px" color="red" face="Helvetica">Lorem ipsum dolor</font>
</div>

#### [`<td bgcolor="">`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-bgcolor)

```html
<table border="1" cellspacing="0">
  <tr>
    <td bgcolor="yellow"> Item 1.1</td>
    <td> Item 1.2</td>
  </tr>
</table>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <table border="1" cellspacing="0" style="display: table;">
    <tr>
      <td bgcolor="yellow"> Item 1.1</td>
      <td> Item 1.2</td>
    </tr>
  </table>
</div>

#### [`<ul type="">`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul#attr-type)

```html
<ul type="square">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <ul type="square">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</div>

## [How to apply your CSS to your HTML](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works#How_to_apply_your_CSS_to_your_HTML)
---

### Inline styles

#### CSS Declaration

```
            declaration
          ┌──────┴───────┐
<p style="font-size: 20px;">Lorem ipsum dolor</p>
          └───┬───┘  └─┬─┘
          property   value
```

#### Example

[`stylesheets/inline/index.html`](stylesheets/inline/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <h1 style="color: blue;">Lorem ipsum</h1>
  <p style="font-size: 20px;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: blue;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: blue;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
</html>  
```

Output:

<div style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: blue;">Lorem ipsum</h1>
  <p style="font-size: 20px;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: blue;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: blue;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

### Internal stylesheet

#### CSS rulesets

```
 selector
   ┌┴┐     declaration
    p { ┌──────┴───────┐
        font-size: 20px;
    }   └───┬───┘  └─┬─┘
        property   value
```

#### Declaration block

```css
p {
  font-size: 20px;
  text-align: justify;
}
```

#### Group of selectors

```css
p, h1 {
  color: blue;
}
```

#### Example

[`stylesheets/internal/index.html`](stylesheets/internal/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <style>
    p {
      font-size: 20px;
      text-align: justify;
    }
    p, h1 {
      color: blue;
    }
  </style>
</head>
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
</html>  
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: blue">Lorem ipsum</h1>
  <p style="font-size: 20px; color: blue; text-align: justify;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="font-size: 20px; color: blue; text-align: justify;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: blue; text-align: justify;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

### External stylesheet

### Structure

```html
<link rel="stylesheet" href="css/master.css">
```

### Example

```
site
├── css
│   └── master.css
└── index.html
```

[`stylesheets/external/index.html`](stylesheets/external/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="css/master.css">
</head>
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
</html>  
```

[`stylesheets/external/css/master.css`](stylesheets/external/css/master.css):
```css
p {
  font-size: 20px;
  text-align: justify;
}
p, h1 {
  color: blue;
}
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: blue">Lorem ipsum</h1>
  <p style="font-size: 20px; color: blue; text-align: justify;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="font-size: 20px; color: blue; text-align: justify;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: blue; text-align: justify;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>


### Mixed stylesheet

```
site
├── css
│   └── master.css
└── index.html
```

[`stylesheets/mixed/index.html`](stylesheets/mixed/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="css/master.css">
  <style>
    p {
      font-size: 20px;
      text-align: justify;
    }
    p, h1 {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Lorem ipsum</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
</html>  
```

[`stylesheets/mixed/css/master.css`](stylesheets/mixed/css/master.css):
```css
p {
  font-size: 17px;
  color: blue;
}
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: red">Lorem ipsum</h1>
  <p style="font-size: 20px; color: green; text-align: justify;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="font-size: 20px; color: red; text-align: justify;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: red; text-align: justify;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

#### CSS Question
> 

> What is the color of the first and last paragraph in the Inline, Internal, External and Mixed Stylesheet? Why?

### References
* [How to apply your CSS to your HTML \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works#How_to_apply_your_CSS_to_your_HTML)
* [Style rule syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Basic_rule_syntax)
* Attributes:
  * [global](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes): `style`
* Elements:
  * [`<link>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link)


## [Properties](https://docs.webplatform.org/wiki/css/properties)
---

### Text Properties

[`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size), 
[`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style), 
[`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight), 
[`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family), 
[`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font)

[property/index.html](property/index.html):
```css
p {
  font-size: 20px;
  font-style: italic;
  font-weight: bold;
  font-family: Times;
}
```

```html
<body>
  <p>Lorem ipsum dolor</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="font: italic bold 20px Times;">Lorem ipsum dolor</p>
</div>

### Shorthand properties

[property/font-shorthand.html](property/font-shorthand.html):
```css
p {
  font: italic bold 20px Times;
}
```
```html
<body>
  <p>Lorem ipsum dolor</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="font: italic bold 20px Times;">Lorem ipsum dolor</p>
</div>

### CSS values and units

#### [`<length>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length)

##### absolute units

```css
p {
  font-size: 17px;
}
```

##### relative units

```css
h1 {
  font-size: 1.3rem;
}

p {
  font-size: 105%;
}
```

| tag | value | computed value |
|-|-|-|
| `body` | 16px | |
| `h1` | 1.3rem | 16.48px |
| `p` | 105% | 16.8px |

#### [`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

```css
h1 {
  color: red;
}

p {
  color: rgb(255, 0, 0);
}
```

### Other Properties

* [Typography](typography.html)
* [Web Font](web-font.html)
* [Icons](icon.html)
* [Hyperlinks](links.html)
* [Box model](box-model.html)
* [Background](background.html)

### References

* Properties:
  * Doc: [WP](https://docs.webplatform.org/wiki/css/properties), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/CSS2/propidx.html)<br>
  * Cheat Sheet: [smashing](https://www.smashingmagazine.com/2009/07/css-3-cheat-sheet-pdf/) ([pdf](https://www.smashingmagazine.com/wp-content/uploads/images/css3-cheat-sheet/css3-cheat-sheet.pdf)), [w3school](http://www.w3schools.com/cssref/), [tutorialspoint](http://www.tutorialspoint.com/css/css_references.htm), [1stwebdesigner](http://www.1stwebdesigner.com/freebies/css-cheat-sheets-designers/)
* Color
  * [Color Table](values.md#color)
  * [CSS values and units \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Values_and_units) (Numeric values, Percentages, Colors, Coordinate positions, Functions)
* [Value definition syntax \| MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Value_definition_syntax)

## [Selectors](https://docs.webplatform.org/wiki/css/selectors)
---

### Group of Selectors 

```css
elementname-1, elementname-2
```

```css
h1, p
```

### Basic selectors

#### Element

[selector/span.html](selector/span.html)
```css
h1 {
  color: blue;
}

span {
  font-weight: bold;
  font-size: 1.2rem;
  color: tomato;
}
```

```html
<h1>Lorem ipsum dolor</h1>
<p>Lorem ipsum, <span>dolor</span> sit amet consectetur adipisicing elit. Id, quia...</p>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: blue;">Lorem ipsum dolor</h1>
  <p>Lorem ipsum, <span style="font-weight: bold; font-size: 1.2rem; color: tomato;">dolor</span> sit amet consectetur adipisicing elit. Id, quia...</p>
</div>

[selector/div.html](selector/div.html)
```css
div {
  color: tomato;
}
```

```html
<h1>Lorem ipsum</h1>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit...</p>
<div>
  <p>Expedita, officia rem, non nulla harum ut fugit optio explicabo temporibus eligendi...</p>
  <p>Perferendis eaque ullam harum illum quas repudiandae dolore minima labore quod...</p>
</div>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: #606c71;">Lorem ipsum dolor</h1>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit...</p>
  <div style="color: tomato;">
    <p>Expedita, officia rem, non nulla harum ut fugit optio explicabo temporibus eligendi...</p>
    <p>Perferendis eaque ullam harum illum quas repudiandae dolore minima labore quod...</p>
  </div>
</div>

#### `#id`

[selector/id.html](selector/id.html):
```css
p {
  color: green;
}

#first {
  color: red;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p id="first">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: #606c71;">Lorem ipsum</h1>
  <p style="color: red;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: green;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="color: green;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

#### `.class`

[selector/class.html](selector/class.html):
```css
p {
  color: green;
}

.red {
  color: red;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p class="red">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p class="red">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: #606c71;">Lorem ipsum</h1>
  <p style="color: red;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: red;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="color: green;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

#### `.class.class`

[selector/classclass.html](selector/classclass.html):
```css
.text-center {
  text-align: center;
}

.red {
  color: red;
}

h1.text-center.red {
  font-size: 3rem;
}
```

```html
<body>
  <h1 class="red text-center">Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p class="red">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

### Combinators

#### `header ul` (Descendant combinator)

[selector/descendant-combinator.html](selector/descendant-combinator.html):
```css
header ul {
  list-style-type: none;
}
```

```html
<body>
  <header>
    <ul>
      <li><a href="#">Menu 1</a></li>
      <li><a href="#">Menu 2</a></li>
    </ul>
  </header>
  <main>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
    </ul>
  </main>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <header>
    <ul style="list-style-type: none;">
      <li><a href="#">Menu 1</a></li>
      <li><a href="#">Menu 2</a></li>
    </ul>
  </header>
  <main>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
    </ul>
  </main>
</div>

#### CSS Question

> What is the selection of `body li`? How many elements?<br>

### Pseudo-class

#### `:hover`

[selector/p-hover.html](selector/p-hover.html)
```css
p:hover {
      font-weight: bold;
    }
```

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta voluptatem ex autem incidunt, aut dolores veritatis nisi repellat perspiciatis nulla reiciendis eum doloribus fugit facere necessitatibus reprehenderit natus libero temporibus.</p>
```

Output:

<iframe src="selector/p-hover.html" width="100%" style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

#### `:first-child`

```css
p:first-child {
  color: green;
}
```

```html
<body>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

![First Child](selector/first-child.png)

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

#### `:nth-child(2)`

```css
p:first-child {
  color: red;
}

p:nth-child(2) {
  color: green;
}
```

```html
<body>
  <h1>Lorem ipsum dolor</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

![nth child](selector/nth-child2.png)

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: #606c71;">Lorem ipsum dolor</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

#### `:nth-child(2n)`

```css
p:nth-child(2n) {
  color: green;
}
```

```html
<body>
  <h1>Lorem ipsum dolor</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p>Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
```

![nth child 2n](selector/nth-child2n.png)

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: #606c71;">Lorem ipsum dolor</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="color: green;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</div>

### CSS Question

> Is it possible to inspect `:hover`?<br>
> Is it possible to replace `:first-child` with `:nth-child`?<br>
> Is it possible to replace general/adjacent sibling combinator selector with `:nth-child`?<br>
> Is it possible to select odd or even elements?<br>

### Pseudo-element

#### `::selection`
[selector/p-selection.html](selector/p-selection.html)
```css
p::selection {
  color: white;
  background-color: grey;
}
```

```html
<h1>Lorem ispsum dolor</h1>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta voluptatem ex autem incidunt, aut dolores veritatis nisi repellat perspiciatis nulla reiciendis eum doloribus fugit facere necessitatibus reprehenderit natus libero temporibus.</p>
```

Output:

<iframe src="selector/p-selection.html" width="100%" style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

### References
* Selectors:
  * Doc: [WP](https://docs.webplatform.org/wiki/css/selectors), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Selectors), W3C ([Level 3](https://www.w3.org/TR/2011/REC-css3-selectors-20110929/#selectors) e [Level 4](https://www.w3.org/TR/2013/WD-selectors4-20130502/#overview))
  * [Selectors Table](selectors.md)
* Attributes:
  * [global](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes): `id`, `class`


## [Functions](https://docs.webplatform.org/wiki/css/functions)
---

### [`rgb()`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#rgb()), [`rgba()`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#rgba())
```css
h1 {
  color: rgb(255, 0, 0);
}

p {
  color: rgba(255, 0, 0, .5);
}
```

### References
* Doc: [WP](https://docs.webplatform.org/wiki/css/functions) e [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)
* [Color Table](values.md#color)

## [At-rules](https://docs.webplatform.org/wiki/css/atrules)
---

### meta-data information

#### [`@import`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40import)
[@import/index.html](@import/index.html)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="css/main.css">
</head>
<body>
  <h1 class="text-center">Lorem ipsum dolor</h1>
  <p class="blue">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
</body>
</html>
```

[@import/css/main.css](@import/css/main.css)
```css
@import url('_color.css');
@import url('_text.css');
```

[@import/css/_color.css](@import/css/_color.css)
```css
.blue {
  color: blue;
}

.red {
  color: red;
}

.green {
  color: green;
}
```

[@import/css/_text.css](@import/css/_text.css)
```css
.text-center {
  text-align: center;
}

.text-left {
  text-align: left;
}

.text-right {
  text-align: right;
}
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="text-align: center;">Lorem ipsum dolor</h1>
  <p style="color: blue;">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
</div>

#### [`@charset`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40charset)

```css
@charset "utf-8";

p {
  color: green;
}
```

### conditional information

(nested statements / conditional group rules / rulesets)

#### [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40media)

```css
p {
  text-align: center;
}

@media print {
  p {
    text-align: left;
  }
}
```

#### [`@document`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40document)

Functions:
* `url()`, `url-prefix()`, `domain()`, `regexp()`

```css
@document url(http://www.w3.org/) {
  p {
    color: red;
  }
}
```

#### [`@support`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40supports)

```css
@supports (--main-color: green;) {
  :root {
    --main-color: green;
  }

  body {
    color: var(--varName);
  }
}
```

### descriptive information

#### [`@font-face`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40font-face)

reference:
- [Web Font Guide](web-font.md)

```css
@font-face {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/roboto/v18/KFOmCnqEu92Fr1Mu72xKKTU1Kvnz.woff2) format('woff2');
}

p {
  font-family: 'Roboto', sans-serif;
}
```

### References
* Doc: [WP](https://docs.webplatform.org/wiki/css/atrules) e [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule)

## [Media Queries](https://docs.webplatform.org/wiki/css/mediaqueries)
---

### Syntax
* [Media types](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_types): `all`, `print`, `screen`, `speech`
* [Media features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features): `width`, `height`, `orientation`
* [Logical operators](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Logical_operators): `and`, `not`, `only`

### Examples

```css
@media print {
  /* rulesets */
}
@media screen {
  /* rulesets */
}
@media screen, print {
  /* rulesets */
}
@media screen and (min-width: 500px) {
  /* rulesets */
}
```

```css
@import 'style.css' print;
@import 'style.css' screen;
@import 'style.css' screen, print;
@import 'style.css' screen and (min-width: 500px);
```

```html
<link rel="stylesheet" href="style.css" media="print">
<link rel="stylesheet" href="style.css" media="screen">
<link rel="stylesheet" href="style.css" media="screen, print">
<link rel="stylesheet" href="style.css" media="screen and (min-width: 500px)">
```

### Responsive Design

```css
/* rulesets */

@media screen and (min-width: 500px) {
  /* rulesets */
}

@media screen and (min-width: 1000px) {
  /* rulesets */
}
```

### References
* Doc: [WP](https://docs.webplatform.org/wiki/css/mediaqueries), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/2012/REC-css3-mediaqueries-20120619/)


## [Comments](https://developer.mozilla.org/en-US/docs/Web/CSS/Comments)
---

```css
/* header */
h1 {
  color: green;
}

/* Content */
p {
  color: blue;
}
```

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <!-- Header -->
  <h1>Lorem ipsum</h1>

  <!-- Content -->
  <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
</body>
</html>
```

## [Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)
---

[inheritance/index.html](inheritance/index.html):
```css
body {
  color: green;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: green;">Lorem ipsum</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: green;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</div>

[inheritance/not-inheritance.html](inheritance/not-inheritance.html):
```css
body {
  color: green;
}
h1 {
  color: red;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: red;">Lorem ipsum</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: green;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</div>

### References
* [Inheritance \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)
* [CSS 2.2 Specification - Appendix F. Full property table (Inherited?)](https://www.w3.org/TR/CSS22/propidx.html)

## References
---

* CSS
  * CSS Awesome [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sotayamashita/awesome-css)
  * Portais: [W3C](https://www.w3.org/standards/webdesign/htmlcss), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) e  [WP](https://docs.webplatform.org/wiki/css)
  * Guias: [MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS) e [WP](https://docs.webplatform.org/wiki/css/tutorials)
  * Padrões: [Notícias](https://www.w3.org/Style/CSS/Overview.en.html), [CSS Current Status](https://www.w3.org/standards/techs/css#w3c_all), [CSS Specifications](https://www.w3.org/Style/CSS/specs.en.html)
  * Versões: [Draft](https://www.w3.org/TR/CSS/), [2](https://www.w3.org/TR/CSS2/), [Outros](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS3)
  * [How CSS Works \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works)
  * [History of HTML & CSS](http://www.wdtonline.com/wdtMagazine/MemberWorks/WiserWays/csshtml.htm)
* Design
  * [Flat Design](https://en.wikipedia.org/wiki/Flat_design)
  * [Material Design](http://www.google.com/design/spec/material-design/introduction.html): [Icons](https://materialdesignicons.com/), [Cores](http://www.materialui.co/), [Exemplos](http://www.materialup.com/),  [Bootstrap](http://fezvrasta.github.io/bootstrap-material-design/), [Materialize CSS](http://materializecss.com/), [getmdl](https://getmdl.io/), [Material UI](http://www.material-ui.com/)
  * [Google Design ](https://design.google.com/)
  * [Metro Design](https://www.microsoft.com/en-us/stories/design/): [MetroUI](https://metroui.org.ua/), [Exemplos](http://theultralinx.com/2013/04/15-metro-design-examples/)
  * Dicas, Tendências e Conceitos
    * [Material vs Flat](http://designmodo.com/flat-vs-material/)
    * [9 Graphic Design Trends](https://designschool.canva.com/blog/design-trends-2016/)
* Preprocessor:
  * [Sass](http://sass-lang.com/)
  * [PostCSS](http://postcss.org/)
* Framework:
  * [Top CSS frameworks to follow in 2017](https://medium.com/@thomasmarciniak/top-css-frameworks-to-follow-in-2017-51d283dd00fb)
  * [Popular CSS Libraries](http://cssdb.co/)
  * [Bootsrap](http://getbootstrap.com/) ([cheat sheet](http://hackerthemes.com/bootstrap-cheatsheet/))
  * [Foundation](http://foundation.zurb.com/)
  * [PureCSS](http://purecss.io/)
  * [Bulma](https://bulma.io)
  * [Materialize CSS](http://materializecss.com/)
  * [SemanticUI](http://semantic-ui.com/)
