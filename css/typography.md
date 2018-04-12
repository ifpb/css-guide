# Typography

## Text and Font
---

References:
- [CSS 2.2 Text \| W3C](https://www.w3.org/TR/CSS22/text.html)
- [CSS 2.2 Font \| W3C](https://www.w3.org/TR/CSS22/fonts.html)
- [Fundamental text and font styling](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)

### [Color](https://developer.mozilla.org/en-US/docs/Web/CSS/color)

> Values: [`<color>`](values.md#color)

#### Syntax

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

#### Example

### [Font family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)

> Values: [[ `<family-name>` | `<generic-family>` ] [, [ `<family-name>`| `<generic-family>`] ]* ] | `inherit`<br>
><br>
>`<family-name>` = `<string>`<br>
>`<generic-family>` = serif | sans-serif | cursive | fantasy | monospace<br>

#### Syntax

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

#### Generic family

References:
- [Font Family](https://www.w3.org/Style/Examples/007/fonts.en.html)
- [Top 30 Best Sans Serif Fonts](http://www.vectordiary.com/fonts/top-30-best-sans-serif-fonts/)
- [Top 30 Best Serif Fonts](http://www.vectordiary.com/fonts/top-30-best-serif-fonts/)
- [Top 30 Modern Fonts](http://www.vectordiary.com/fonts/top-30-modern-fonts/)


<div style="font-size: 2rem;">
  <span style="font-family: serif">Lorem</span>
  <span style="font-family: sans-serif">Lorem</span>
  <span style="font-family: monospace">Lorem</span>
  <span style="font-family: cursive">Lorem</span>
  <span style="font-family: fantasy">Lorem</span>
</div>

| `<generic-family>` | `<family-name>` |
|-|-|
| serif | Times, Times New Roman, Georgia, Century, Lucida, Didot |
| sans-serif | Arial, Arial Black, Open Sans, Lucida Sans, Trebuchet MS, Verdana, Helvetica, Helvetica Neue, Gill Sans, Futura, San Fransisco, Tahoma, Ubuntu |
| monospace | Courier, Courier New, Andale Mono, Monaco |
| cursive | Brush Script MT, Zapfino, Comic Sans MS, Bradley Hand |
| fantasy | Impact, Papyrus, Luminari, Chalkduster, Chalkboard, Marker Felt, Trattatello, Cochin |

[Outros](https://www.w3.org/Style/Examples/007/fonts.en.html#font-family)

#### Default fonts

| `<generic-family>` | Preview |
|-|-|
| serif | <span style="font-family: serif">Lorem ipsum</span> |
| sans-serif | <span style="font-family: sans-serif">Lorem ipsum</span> |
| monospace | <span style="font-family: monospace">Lorem ipsum</span> |
| cursive | <span style="font-family: cursive">Lorem ipsum</span> |
| fantasy | <span style="font-family: fantasy">Lorem ipsum</span> |

> Chrome > settings > Appearance > Customize fonts

#### Web safe fonts

| `<family-name>` | `<generic-family>` | Preview |
|-|-|-|
| Times New Roman | serif | <span style="font-family: Times New Roman, serif">Lorem ipsum</span> |
| Georgia | serif | <span style="font-family: Georgia, serif">Lorem ipsum</span> |
| Arial | sans-serif | <span style="font-family: Arial, sans-serif">Lorem ipsum</span> |
| Arial Black | sans-serif | <span style="font-family: Arial Black, sans-serif">Lorem ipsum</span> |
| Trebuchet MS | sans-serif | <span style="font-family:  Trebuchet MS, sans-serif">Lorem ipsum</span> |
| Verdana | sans-serif | <span style="font-family: Verdana, sans-serif">Lorem ipsum</span> |
| Courier New | monospace | <span style="font-family: Courier New, monospace">Lorem ipsum</span> |
| Andale Mono | monospace | <span style="font-family: Andale Mono, monospace">Lorem ipsum</span> |
| Brush Script MT | cursive | <span style="font-family: Brush Script MT, monospace">Lorem ipsum</span> |
| Comic Sans MS | cursive | <span style="font-family: Comic Sans MS, sans-serif">Lorem ipsum</span> |
| Impact | fantasy | <span style="font-family: Impact, sans-serif">Lorem ipsum</span> |
|  Webdings | fantasy | <span style="font-family:  Webdings, sans-serif">Lorem ipsum</span> |
Font: [Core fonts for the Web](https://en.wikipedia.org/wiki/Core_fonts_for_the_Web)

#### Font stacks / Fallback

```css
body {
  font-family: Ubuntu, Arial, sans-serif;
}
```

#### Example

### [Font size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)

> Values: \[ `<absolute-size>` \| `<relative-size>` \| `<length-percentage>` \]<br>
><br>
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

### [`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)

> Values: normal \| italic \| oblique

```css
font-style: normal;
font-style: italic;
font-style: oblique;
```

### [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)

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

### [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

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

### [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

Values: text-decoration-line, text-decoration-color, and text-decoration-style

>where<br>
> text-decoration-line = none | [ underline || overline || line-through || blink ]<br>

```css
/* Keyword values */
text-decoration: none;                /* No text decoration */
text-decoration: underline red;       /* Red underlining */
text-decoration: underline wavy red;  /* Red wavy underlining */
```

### [`text-indent`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent)

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

### [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)

Values: none \| capitalize \| uppercase \| lowercase \| full-width

```css
/* Keyword values */
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: none;
text-transform: full-width;
```

<!-- TODO
[`simple-text-style/index.html`](simple-text-style/index.html) 
* [Cap Drops](https://css-tricks.com/snippets/css/drop-caps/) 
icon
web font
print
-->