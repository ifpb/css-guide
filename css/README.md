# CSS

* [Hello World](#hello-world)
* [How to apply your CSS to your HTML](#how-to-apply-your-css-to-your-html)
  * [Inline stylesheet](#inline-stylesheet)
  * [Internal stylesheet](#internal-stylesheet)
  * [External stylesheet](#external-stylesheet)
  * [Mixed stylesheet](#mixed-stylesheet)
* [Inheritance & Cascade](#inheritance--cascade)
  * [Properties](#properties)
    * [Typography](#typography):
      * [`color`](#color)
      * [`font-size`](#font-size)
      * [`font-family`](#font-family)
      * [`font-style`](#font-style)
      * [`font-weight`](#font-weight)
      * [`text-align`](#text-align)
      * [`text-decoration`](#text-decoration)
      * [`text-indent`](#text-indent)
      * [`text-transform`](#text-transform)
    * [Line](#line):
      * [`line-height`](#line-height)
    * [Background](#background):
      * [`background`](#background-1)
      * [`background-attachment`](#background-attachment)
      * [`background-color`](#background-color)
      * [`background-image`](#background-image)
      * [`background-position`](#background-position)
      * [`background-repeat`](#background-repeat)
      * [`background-size`](#background-size)
    * [Box Model](#box-model):
      * [`margin`](#margin)
      * [`padding`](#padding)
      * [`width`](#width)
      * [`height`](#height)
      * [`display`](#display)
    * [Border](#border):
      * [`border`](#border-1)
      * [`border-colapse`](#border-colapse)
      * [`border-color`](#border-color)
      * [`border-style`](#border-style)
      * [`border-width`](#border-width)
      * [`border-radius`](#border-radius)
      * [`box-shadow`](#box-shadow)
    * [Line Box](#line-box):
      * [`vertical-align`](#vertical-align)
    * [User Interface](#user-interface):
      * [`cursor`](#cursor)
* [Selectors](#selectors)
* [Functions](#functions)
* [At-rules](#at-rules)
* [Media Queries](#media-queries)
* [Values](#values)
  * [`<color>`](#color-1)
* [Effects](#effects)
* [Links Úteis](#links-uteis)

## References
---

* CSS Awesome [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sotayamashita/awesome-css)<br>
* Portais: [W3C](https://www.w3.org/standards/webdesign/htmlcss), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) e  [WP](https://docs.webplatform.org/wiki/css)<br>
* Guias: [MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS) e [WP](https://docs.webplatform.org/wiki/css/tutorials)<br>
* Padrões: [Notícias](https://www.w3.org/Style/CSS/Overview.en.html), [CSS Current Status](https://www.w3.org/standards/techs/css#w3c_all), [CSS Specifications](https://www.w3.org/Style/CSS/specs.en.html)<br>
* Versões: [Draft](https://www.w3.org/TR/CSS/), [2](https://www.w3.org/TR/CSS2/), [Outros](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS3)<br>
* [How CSS Works \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works)<br>

## Hello World
---

[`hello/index.html`](hello/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <p style="color:blue;font-size:20px;">Olá, mundo!</p>
</body>
</html>
```  

## How to apply your CSS to your HTML
---

MDN: [How to apply your CSS to your HTML](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works#How_to_apply_your_CSS_to_your_HTML)

### Inline stylesheet

[`index.html`](stylesheets/inline/index.html) ([Style rule syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Basic_rule_syntax)):

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <h1>Lorem ipsum</h1>
  <p style="font-size: 20px;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: blue;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
  <p style="font-size: 20px; color: blue;">Culpa possimus obcaecati laudantium nesciunt consequatur...</p>
</body>
</html>  
```

### Internal stylesheet

[`index.html`](stylesheets/internal/index.html):

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <style>
    p {
      font-size: 17px;
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

### External stylesheet

```
site
├── css
│   └── master.css
└── index.html
```

[`index.html`](stylesheets/external/index.html):
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

[`css/master.css`](stylesheets/external/css/master.css):
```css
p {
  font-size: 17px;
  color: blue;
}
```

### Mixed stylesheet

```
site
├── css
│   └── master.css
└── index.html
```

[`index.html`](stylesheets/mixed/index.html):
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="css/master.css">
  <style>
    p {
      font-size: 17px;
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

[`css/master.css`](stylesheets/mixed/css/master.css):
```css
p {
  font-size: 17px;
  color: blue;
}
```

### CSS Questions

> What is the color of the first and last paragraph in the Inline, Internal, External and Mixed Stylesheet?

## Inheritance & Cascade
---

Reference: [W3C](https://www.w3.org/TR/CSS22/cascade.html), [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance), [WP](https://docs.webplatform.org/wiki/tutorials/inheritance_and_cascade)<br>
User style sheet: Stylish ([Plugin](https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe?hl=en) & [Gallery](http://userstyles.org/))<br>

## Properties
---

References: [WP](https://docs.webplatform.org/wiki/css/properties), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/CSS2/propidx.html)<br>
Cheat Sheet: [smashing](https://www.smashingmagazine.com/2009/07/css-3-cheat-sheet-pdf/) ([pdf](https://www.smashingmagazine.com/wp-content/uploads/images/css3-cheat-sheet/css3-cheat-sheet.pdf)), [w3school](http://www.w3schools.com/cssref/), [tutorialspoint](http://www.tutorialspoint.com/css/css_references.htm), [1stwebdesigner](http://www.1stwebdesigner.com/freebies/css-cheat-sheets-designers/))<br>

### Typography

Ícones: [material icons](https://material.io/icons/), [font-awesome](http://fontawesome.io), [flat icon](https://www.flaticon.com), [material design icons](https://materialdesignicons.com)<br>

#### Examples

[`simple-text-style/index.html`](simple-text-style/index.html)

#### [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)

Values: &lt;color>

```css
/* <named-color> values */
color: red;

/* <hex-color> values */
color: #009900;

/* <rgb()> values */
color: rgb(34, 12, 64, 0.6);

/* <hsl()> values */
color: hsl(30, 100%, 50%, 0.6);
```

#### [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)

Values: \[ &lt;absolute-size> \| &lt;relative-size> \| &lt;length-percentage> \]

>where<br>
>&lt;absolute-size> = xx-small | x-small | small | medium | large | x-large | xx-large<br>
>&lt;relative-size> = larger | smaller<br>
>&lt;length-percentage> = &lt;length> | &lt;percentage>

```css
/* <absolute-size> values */
font-size: xx-small;
font-size: x-small;
font-size: small;
font-size: medium;
font-size: large;
font-size: x-large;
font-size: xx-large;

/* <relative-size> values */
font-size: smaller;
font-size: larger;

/* <length> values */
font-size: 12px;
font-size: 0.8em;

/* <percentage> values */
font-size: 80%;
```

#### [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)

Values: \[ &lt;family-name> \| &lt;generic-family> \]

>where <br>
>&lt;family-name> = <string> | &lt;custom-ident>+<br>
>&lt;generic-family> = serif | sans-serif | cursive | fantasy | monospace // Fallback<br>

```css
/* A font family name and a generic family name */
font-family: Gill Sans Extrabold, sans-serif;
font-family: "Goudy Bookletter 1911", sans-serif;

/* A generic family name only */
font-family: serif;
font-family: sans-serif;
font-family: monospace;
font-family: cursive;
font-family: fantasy;
font-family: system-ui;
```

#### [`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)

Values: normal \| italic \| oblique

```css
font-style: normal;
font-style: italic;
font-style: oblique;
```

#### [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)

Values: normal \| bold \| bolder \| lighter \| 100 \| 200 \| 300 \| 400 \| 500 \| 600 \| 700 \| 800 \| 900

```css
/* Keyword values */
font-weight: normal;
font-weight: bold;

/* Keyword values relative to the parent */
font-weight: lighter;
font-weight: bolder;

/* Numeric keyword values */
font-weight: 100;
font-weight: 200;
font-weight: 300;
font-weight: 400;
font-weight: 500;
font-weight: 600;
font-weight: 700;
font-weight: 800;
font-weight: 900;
```

#### [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

Values: start \| end \| left \| right \| center \| justify \| match-parent

```css
/* Keyword values */
text-align: left;
text-align: right;
text-align: center;
text-align: justify;
text-align: justify-all;
text-align: start;
text-align: end;
text-align: match-parent;
```

#### [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

Values: text-decoration-line, text-decoration-color, and text-decoration-style

>where<br>
> text-decoration-line = none | [ underline || overline || line-through || blink ]<br>

```css
/* Keyword values */
text-decoration: none;                /* No text decoration */
text-decoration: underline red;       /* Red underlining */
text-decoration: underline wavy red;  /* Red wavy underlining */
```

#### [`text-indent`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent)

Values: &lt;length-percentage> && hanging? && each-line?

> where <br>
> &lt;length-percentage> = &lt;length> | &lt;percentage>

```css
/* <length> values */
text-indent: 3mm;
text-indent: 40px;

/* <percentage> value
   relative to the containing block width */
text-indent: 15%;

/* Keyword values */
text-indent: 5em each-line;
text-indent: 5em hanging;
text-indent: 5em hanging each-line;
```

#### [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)

Values: none \| capitalize \| uppercase \| lowercase \| full-width

```css
/* Keyword values */
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: none;
text-transform: full-width;
```

### Line

#### [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)

### Background

[Strip Generator](http://www.stripegenerator.com/)<br>
[Gradient](http://www.generateit.net/gradient/index.php)<br>
[Imagens](http://www.freepik.com/free-vectors/background)<br>
Sprite CSS<br>

#### [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background)

Values: &lt;attachment> &lt;box> &lt;background-color> &lt;bg-image> &lt;position> &lt;repeat-style> &lt;bg-size>

#### [`background-attachment`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)

Values: fixed \| scrool

#### [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)

Values: &lt;color>

#### [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)

Values: none \| &lt;image>

#### [`background-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)

Values: &lt;position>

#### [`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat)

Values: &lt;repeat-style> (repeat \| repeat-x \| repeat-y \| no-repeat)

#### [`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size)

Values: contain \| cover \| auto \| &lt;length> \| &lt;percentage>

### Box Model

#### [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)

#### [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

#### [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)

#### [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height)

#### [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

### Border

#### [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

#### [`border-colapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-colapse)

#### [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color)

#### [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)

#### [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)

#### [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

#### [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)

### Line Box

#### [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)

### User Interface

#### [`cursor`](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor)

## Selectors
---

<!-- TODO graphich, samples, obs -->

References: [WP](https://docs.webplatform.org/wiki/css/selectors), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Selectors), W3C ([Level 3](https://www.w3.org/TR/2011/REC-css3-selectors-20110929/#selectors) e [Level 4](https://www.w3.org/TR/2013/WD-selectors4-20130502/#overview))

### [Basic selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors#Basic_selectors)
Grouping `elementname-1, elementname-2`<br>

#### [Type selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors) `elementname`

#### [Class selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) `.classname`

#### [ID selector](https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) `#idname`

#### [Universal selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors) `*`

#### [Attribute selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) `[attr]`, `[attr=value]`, `[attr~=value]`, `[attr|=value]`, `[attr^=value]`, `[attr$=value]`, `[attr*=value]`

### [Combinators](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors#Combinators)

#### [Adjacent sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_selectors) `A + B`

#### [General sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_selectors) `A ~ B`

#### [Child combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_selectors) `A > B`

#### [Descendant combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_selectors) `A B`

### [Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

#### [`:active`](https://developer.mozilla.org/en-US/docs/Web/CSS/:active)

#### [`:checked`](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)

#### [`:focus`](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)

#### [`:first-child`](https://developer.mozilla.org/en-US/docs/Web/CSS/:first-child)

> Observação<br>
> 1. É possível descrever este pseudo-class usando `:nth-child`

#### [`:hover`](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)

#### [`:last-child`](https://developer.mozilla.org/en-US/docs/Web/CSS/:last-child)

#### [`:link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:link)

#### [`:nth-child`](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)

> Observação<br>
> 1. Este pseudo-class pode se comportar como type selector?
> 1. Este pseudo-class pode se comportar como `:first-child`?
> 4. Este pseudo-class pode se comporatar como general/adjacent sibling combinator selector?
> 2. Como se selecionar apenas elementos de 2 em 2, ou de 3 em 3?
> 3. É possível trazer os elementos pares ou ímpares?

#### [`:nth-of-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type)

#### [`:visited`](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited)

### [Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

#### [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)

#### [`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)

#### [`::first-letter`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)

#### [`::first-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-line)

#### [`::selection`](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection)

## Functions
---

References: [WP](https://docs.webplatform.org/wiki/css/functions) e [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)

## At-rules
---

References: [WP](https://docs.webplatform.org/wiki/css/atrules) e [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule)

`@font-face` (`src`, `font-family`)<br>
`@media`

## Media Queries
---

References: [WP](https://docs.webplatform.org/wiki/css/mediaqueries), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/2012/REC-css3-mediaqueries-20120619/)

media: `print`, `screen`

## Values
---

#### [`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

**[Color Keyword](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#Color_keywords)**

```css
/* <named-color> values */
color: white;
color: black;
color: red;
color: green;
color: blue;
color: cyan;
color: rebeccapurple;

/* <hex-color> values */
color: #ffffff;
color: #000000;
color: #ff0000;
color: #00ff00;
color: #0000ff;
color: #00ffff;
color: #663399;
color: #639;
color: #66339977;
color: #6397;

/* <rgb()> values */
color: rgb(255, 255, 255)
color: rgb(0, 0, 0)
color: rgb(255, 0, 0)
color: rgb(0, 255, 0)
color: rgb(0, 0, 255)
color: rgb(0, 255, 255)
color: rgb(102, 51, 153)
color: rgba(102, 51, 153, 0.5);

/* <hsl()> values */
color: hsl(0, 0%, 100%);
color: hsl(0, 0%, 0%);
color: hsl(0, 100%, 50%);
color: hsl(120, 100%, 50%);
color: hsl(240, 100%, 50%);
color: hsl(180, 100%, 50%);
color: hsl(270, 50%, 40%);
color: hsla(270, 50%, 40%, 0.5);
```

| &lt;named-color&gt; values | &lt;hex-color> values<br>(#rrggbb & [#rrggbbaa](https://caniuse.com/#feat=css-rrggbbaa)) | &lt;rgb()> values | [&lt;hsl()> values](https://en.wikipedia.org/wiki/HSL_and_HSV) |
|-|-|-|-|
| <span style="color: white">white</span> | <span style="color: #ffffff">#ffffff</span> | <span style="color: rgb(255, 255, 255)">rgb(255, 0, 0)</span> | <span style="color: hsl(0, 0%, 100%)"> hsl(0, 0%, 100%)</span> |
| <span style="color: black">black</span> | <span style="color: #000000">#000000</span> | <span style="color: rgb(0, 0, 0)">rgb(0, 0, 0)</span> | <span style="color: hsl(0, 0%, 0%)"> hsl(0, 0%, 0%)</span> |
| <span style="color: red">red</span> | <span style="color: #ff0000">#ff0000</span> | <span style="color: rgb(255, 0, 0)">rgb(255, 0, 0)</span> | <span style="color: hsl(0, 100%, 50%)"> hsl(0, 100%, 50%)</span> |
| <span style="color: green">green</span> | <span style="color: #00ff00">#00ff00</span> | <span style="color: rgb(0, 255, 0)">rgb(0, 255, 0)</span> | <span style="color: hsl(120, 100%, 50%)"> hsl(120, 100%, 50%)</span> |
| <span style="color: blue">blue</span> | <span style="color: #0000ff">#0000ff</span> | <span style="color: rgb(0, 0, 255)">rgb(0, 0, 255)</span> | <span style="color: hsl(240, 100%, 50%)"> hsl(240, 100%, 50%)</span> |
| <span style="color: cyan">cyan</span> | <span style="color: #00ffff">#00ffff</span> | <span style="color: rgb(0, 255, 255)">rgb(0, 255, 255)</span> | <span style="color: hsl(180, 100%, 50%)"> hsl(180, 100%, 50%)</span> |
| <span style="color: rebeccapurple">rebeccapurple</span> | <span style="color: #663399">#663399</span> <span style="color: #639">#639</span> | <span style="color: rgb(102, 51, 153)">rgb(102, 51, 153)</span><br><span style="color: rgba(102, 51, 153, 1)">rgba(102, 51, 153, 1)</span> | <span style="color: hsl(270, 50%, 40%)"> hsl(270, 50%, 40%)</span><br><span style="color: hsla(270, 50%, 40%, 1)"> hsla(270, 50%, 40%, 1)</span> |
| <span style="color: rgba(102, 51, 153, 0.5)">rebeccapurple 50%</span> | <span style="color: #66339977">#66339977</span> <span style="color: #6397">#6397</span> | <span style="color: rgba(102, 51, 153, 0.5)">rgba(102, 51, 153, 0.5)</span> | <span style="color: hsla(270, 50%, 40%, 0.5)"> hsla(270, 50%, 40%, 0.5)</span> |

**Tools**
- [Chrome DevTools: Color Picker](https://developers.google.com/web/tools/chrome-devtools/css/reference#color-picker)
- Color Info
  - Tools
    - [rgbTo](http://rgb.to/)
    - [color-hex](http://www.color-hex.com/)
    - [colourco](http://www.colourco.de/)
    - Google Search
  - #663399 Color Hex Rebecca Purple Info
    - [color-hex](http://www.color-hex.com/color/663399)
      - Shades of #663399
      - Tints of #663399
      - Triadic Colors of #663399
      - Analogous Colors of #663399
      - Monochromatic Colors of #663399
      - Complementary Color of #663399
      - Related Colors of #663399
    - [rgbTo](http://rgb.to/rgb/102,51,153)

**[Color Model](https://en.wikipedia.org/wiki/Color_model)**
- [RGB](https://en.wikipedia.org/wiki/RGB_color_model) (additive color model)
- [CMYK](https://en.wikipedia.org/wiki/CMYK_color_model) (subtractive color model)

**Pastel Color**

## Effects
---

* Counters CSS: [CSS Tricks](https://css-tricks.com/numbering-in-style/) e [Nested](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Lists_and_Counters/Using_CSS_counters)
* [Cap Drops](https://css-tricks.com/snippets/css/drop-caps/)

## Links Úteis
---

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
  * [Bootsrap](http://getbootstrap.com/) ([cheat sheet](http://hackerthemes.com/bootstrap-cheatsheet/))
  * [Foundation](http://foundation.zurb.com/)
  * [PureCSS](http://purecss.io/)
  * [Materialize CSS](http://materializecss.com/)
  * [SemanticUI](http://semantic-ui.com/)

<!-- TODO
https://mdn.mozillademos.org/files/9461/css-declaration-small.png
https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics

https://github.com/mdn/beginner-html-site-styled (html; css)
 -->