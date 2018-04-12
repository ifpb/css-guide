# Typography

## Text and Font
---

References:
- [CSS 2.2 Text \| W3C](https://www.w3.org/TR/CSS22/text.html)
- [CSS 2.2 Font \| W3C](https://www.w3.org/TR/CSS22/fonts.html)
- [Fundamental text and font styling](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)

### [Color](https://developer.mozilla.org/en-US/docs/Web/CSS/color)

> <b>Values:</b> [`<color>`](values.md#color)

#### Syntax

```css
/* <named-color> value */
color: red;

/* <hex-color> value */
color: #009900;

/* <rgb-color> value */
color: rgb(34, 12, 64, .6);

/* <hsl-color> value */
color: hsl(30, 100%, 50%, .6);
```

#### Example

| Style | Style | Preview |
|-|-|-|
| color: tomato; | `<named-color>` | <span style="color: tomato">Lorem ipsum</span> |
| color: #FF6347; | `<hex-color>` | <span style="color: #FF6347">Lorem ipsum</span> |
| color: rgb(255,99,71); | `<rgb-color>` | <span style="color: rgb(255,99,71)">Lorem ipsum</span> |
| color: hsl(9, 100%, 64%); | `<hsl-color>` | <span style="color: hsl(9, 100%, 64%)">Lorem ipsum</span> |
| color: rgba(255,99,71, .6); | `<rgba-color>` | <span style="color: rgba(255,99,71, .6)">Lorem ipsum</span> |

Fonte: [Tomato Color](http://www.color-hex.com/color/ff6347)

### [Font family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)

> <b>Values:</b> [[ [`<family-name>`](values.md#family-name) | [`<generic-family>`](values.md#generic-family) ] [, [ [`<family-name>`](values.md#family-name) | [`<generic-family>`](values.md#generic-family)] ]* ] | `inherit`<br>
><br>
>[`<family-name>`](values.md#family-name) = `<string>`<br>
>[`<generic-family>`](values.md#generic-family) = serif | sans-serif | cursive | fantasy | monospace<br>

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

#### Font stacks / Fallback

```css
body {
  font-family: Ubuntu, Arial, sans-serif;
}
```

#### Example

| Style | Syntax | Preview |
|-|-|-|
| font-family: serif; | `<generic-family>` | <span style="font-family: serif">Lorem ipsum</span> |
| font-family: Times, serif; | `<family-name>`, `<generic-family>` | <span style="font-family: Times, serif;">Lorem ipsum</span> |
| font-family: "Time New Roman", serif; | `<family-name>`, `<generic-family>`  | <span style="font-family: 'Time New Roman', serif;">Lorem ipsum</span> |
| font-family: Ubuntu, Arial, sans-serif; | `<family-name>`, `<family-name>`, `<generic-family>`  | <span style="font-family: font-family: Ubuntu, Arial, sans-serif;">Lorem ipsum</span> |

### [Font size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)

> <b>Values:</b> [ `<absolute-size>` | `<relative-size>` | [`<length>`](values.md#length) | `<percentage>` | inherit ]<br>
><br>
>`<absolute-size>` = xx-small | x-small | small | medium | large | x-large | xx-large<br>
>`<relative-size>` = larger | smaller<br>

#### Syntax

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
font-size: 0.8rem;

/* <percentage> values */
font-size: 80%;
```

#### Example

| Style | Syntax | Preview |
|-|-|-|
| font-size: small; | `<abosolut-size>` | <span style="font-size: small;">Lorem ipsum</span> |
| font-size: large; | `<abosolut-size>` | <span style="font-size: large;">Lorem ipsum</span> |
| font-size: larger; | `<relative-size>` | <span style="font-size: larger;">Lorem ipsum</span> |
| font-size: 16px; | `<length>` | <span style="font-size: 16px;">Lorem ipsum</span> |
| font-size: 1.5rem; | `<length>` | <span style="font-size: 1.5rem;">Lorem ipsum</span> |
| font-size: 1.5em; | `<length>` | <span style="font-size: 1.5em;">Lorem ipsum</span> |
| font-size: 150%; | `<percentage>` | <span style="font-size: 150%;">Lorem ipsum</span> |

### [Font style](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)

> <b>Values:</b> normal \| italic \| oblique \| inherit

#### Syntax

```css
font-style: normal;
font-style: italic;
font-style: oblique;
```

#### Example

| Style | Preview |
|-|-|-|
| font-style: normal; | <span style="font-style: normal;">Lorem ipsum</span> |
| font-style: italic; | <span style="font-style: italic;">Lorem ipsum</span> |
| font-style: oblique; | <span style="font-style: oblique;">Lorem ipsum</span> |


### [Font weight](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)

> <b>Values:</b> normal \| bold \| bolder \| lighter \| 100 \| 200 \| 300 \| 400 \| 500 \| 600 \| 700 \| 800 \| 900

#### Syntax

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

#### Example

| Style | Preview |
|-|-|-|
| font-weight: normal; | <span style="font-weight: normal;">Lorem ipsum</span> |
| font-weight: bold; | <span style="font-weight: bold;">Lorem ipsum</span> |
| font-weight: lighter; | <span style="font-weight: lighter;">Lorem ipsum</span> |
| font-weight: bolder; | <span style="font-weight: bolder;">Lorem ipsum</span> |
| font-weight: 100; | <span style="font-weight: 100;">Lorem ipsum</span> |
| font-weight: 200; | <span style="font-weight: 200;">Lorem ipsum</span> |
| font-weight: 300; | <span style="font-weight: 300;">Lorem ipsum</span> |
| font-weight: 400; | <span style="font-weight: 400;">Lorem ipsum</span> |
| font-weight: 500; | <span style="font-weight: 500;">Lorem ipsum</span> |
| font-weight: 600; | <span style="font-weight: 600;">Lorem ipsum</span> |
| font-weight: 700; | <span style="font-weight: 700;">Lorem ipsum</span> |
| font-weight: 800; | <span style="font-weight: 800;">Lorem ipsum</span> |
| font-weight: 900; | <span style="font-weight: 900;">Lorem ipsum</span> |


### [Text align](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

> <b>Values:</b> start \| end \| left \| right \| center \| justify \| match-parent

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

#### Example

| Style | Preview |
|-|-|
| text-align: left; | <div style="text-align: left; width: 200px">Lorem ipsum dolor amet, consectetur.</div> |
| text-align: center; | <div style="text-align: center; width: 200px">Lorem ipsum dolor amet, consectetur.</div> |
| text-align: right; | <div style="text-align: right; width: 200px">Lorem ipsum dolor amet, consectetur.</div> |
| text-align: justify; | <div style="text-align: justify; width: 200px">Lorem ipsum dolor amet, consectetur.</div> |


### [Text decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

> <b>Values:</b> `<text-decoration-line>` || `<text-decoration-color>` || `<text-decoration-style>`<br>
> <br>
> `<text-decoration-line>` = none | [ underline || overline || line-through || blink ]<br>
> `<text-decoration-color>` = `<color>`<br>
> `<text-decoration-style>` = solid | double | dotted | dashed | wavy<br>

#### Syntax

```css
/* Keyword values */
text-decoration: none;                /* No text decoration */
text-decoration: underline;           /* Underlining */
text-decoration: underline red;       /* Red underlining */
text-decoration: underline wavy red;  /* Red wavy underlining */
```

#### Example

| Style | Preview |
|-|-|-|
| text-decoration: none; | <span style="text-decoration: none;">Lorem ipsum</span> |
| text-decoration: underline; | <span style="text-decoration: underline;">Lorem ipsum</span> |
| text-decoration: line-through; | <span style="text-decoration: line-through;">Lorem ipsum</span> |
| text-decoration: overline; | <span style="text-decoration: overline;">Lorem ipsum</span> |
| text-decoration: underline red; | <span style="text-decoration: underline red;">Lorem ipsum</span> |
| text-decoration: underline red wavy; | <span style="text-decoration: underline red wavy;">Lorem ipsum</span> |


### [Text indent](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent)

> <b>Values:</b> `<length-percentage>`<br>
> <br>
> `<length-percentage>` = `<length>` | `<percentage>`

#### Syntax

```css
/* <length> values */
text-indent: 3mm;
text-indent: 40px;

/* <percentage> value
   relative to the containing block width */
text-indent: 15%;
```

#### Example

| Style | Preview |
|-|-|
| text-indent: 3rem; | <div style="text-indent: 3rem; width: 200px">Lorem ipsum dolor amet, consectetur.</div> |


### [Text transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)

> <b>Values:</b> none \| capitalize \| uppercase \| lowercase \| full-width

#### Syntax

```css
/* Keyword values */
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: none;
text-transform: full-width;
```

#### Example

| Style | Preview |
|-|-|-|
| text-transform: none; | <span style="text-transform: none;">Lorem ipsum</span> |
| text-transform: uppercase; | <span style="text-transform: uppercase;">Lorem ipsum</span> |
| text-transform: lowercase; | <span style="text-transform: lowercase;">Lorem ipsum</span> |
| text-transform: capitalize; | <span style="text-transform: capitalize;">Lorem ipsum</span> |
