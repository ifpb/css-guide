## Typography
---

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