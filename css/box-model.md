# Box Model

* [Box Model](#box-model)
* [Border](#border)
* [Margin](#margin)
* [Padding](#padding)
* [Width](#width)
* [Height](#height)

## Box Model
- [Box model recap](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Box_model_recap)
- [Styling borders using CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Borders)

![Box Model](https://mdn.mozillademos.org/files/13647/box-model-standard-small.png)<br>
Fonte: [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Box_model_recap)

## [Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)


| Display | Flow | Margin, Border, Padding | Height | Width |
|-|-|-|-|-|-|-|
| Inline | surrounding text without creating line breaks before | Ok |  |  |
| Block | stacked upon other boxes | Ok | Ok | Ok |
| Inline-block |  surrounding text without creating line breaks before | Ok | Ok | Ok |

### Inline box

```html
<span>Lorem ipsum</span>
<span>dolor</span>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <span>Lorem ipsum</span>
  <span>dolor</span>
</div>

### Block box

```html
<p>Lorem ipsum</p>
<p>Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p>Lorem ipsum</p>
  <p>Lorem ipsum</p>
</div>

### Inline-block box

```css
ul li {
  display: inline-block;
}
```

```html
<ul>
  <li>Lorem ipsum</li>
  <li>dolor</li>
</ul>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <ul>
    <li style="display: inline-block;">Lorem ipsum</li>
    <li style="display: inline-block;">dolor</li>
  </ul>
</div>

## [Border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

> <b>Value:</b> `<br-width>` || `<br-style>` || `<color>`<br>
> <br>
> `<br-width>` = `<length>` \| thin \| medium \| thick<br>
> `<br-style>` = none \| hidden \| dotted \| dashed \| solid \| double \| groove \| ridge \| inset \| outset

### Syntax
```css
/* style */
border: solid;

/* width | style */
border: 2px dotted;

/* style | color */
border: outset #f33;

/* width | style | color */
border: medium dashed green;
```

### Example

```css
#first {
  border: 2px dotted #000;
}

#last {
  border: 5px solid #000;
}
```

```html
<p id="first">Lorem ipsum</p>
<p id="last">Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 2px dotted #000;">Lorem ipsum</p>
  <p style="border: 5px solid #000;">Lorem ipsum</p>
</div>

### Shorthand and Longhand options

| Shorthand | Longhand |
|-|-|
| [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) | [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)<br>[`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)<br>[`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) | 
| [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width) | [`border-top-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)<br>[`border-right-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-width)<br>[`border-bottom-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-width)<br>[`border-left-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-width) |
| [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style) | [`border-top-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-style)<br>[`border-right-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-style)<br>[`border-bottom-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-style)<br>[`border-left-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-style) |
| [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) | [`border-top-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-color)<br>[`border-right-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-color)<br>[`border-bottom-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-color)<br>[`border-left-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-color) |

## [Margin](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

> <b>Value:</b> [ `<length>` | `<percentage>` | auto ]{1,4}

### Syntax
```css
/* Apply to all four sides */
margin: 1em;
margin: -3px;

/* vertical | horizontal */
margin: 5% auto;

/* top | horizontal | bottom */
margin: 1em auto 2em; 

/* top | right | bottom | left */
margin: 2px 1em 0 auto;
```

### Example

```css
.margin {
  border: 5px dotted #000;
  margin: 3rem;
}
```

```html
<p>Lorem ipsum</p>
<p class="margin">Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p>Lorem ipsum</p>
  <p style="border: 5px solid #000; margin: 3rem;">Lorem ipsum</p>
</div>

### Shorthand and Longhand options

| Shorthand | Longhand |
|-|-|
| [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) | [`margin-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)<br>[`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)<br>[`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)<br>[`margin-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top) |

## [Padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

> <b>Value:</b> [ `<length>` | `<percentage>` ]{1,4}

### Syntax

```css
/* Apply to all four sides */
padding: 1em;

/* vertical | horizontal */
padding: 5% 10%;

/* top | horizontal | bottom */
padding: 1em 2em 2em;

/* top | right | bottom | left */
padding: 5px 1em 0 2em;
```

### Example

```css
p {
  border: 5px solid #000;
  padding: 3rem;
}
```

```html
<p>Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 5px solid #000; padding: 3rem;">Lorem ipsum</p>
</div>

### Shorthand and Longhand options

| Shorthand | Longhand |
|-|-|
| [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) | [`padding-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-bottom)<br>[`padding-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-left)<br>[`padding-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-right)<br>[`padding-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-top) |

## [Width](https://developer.mozilla.org/en-US/docs/Web/CSS/width)

> <b>Value:</b> [ `<length>` | `<percentage>` | auto ]

### Syntax

```css
/* <length> values */
width: 300px;
width: 25em;

/* <percentage> value */
width: 75%;
```

### Example

```css
p {
  border: 5px solid #000;
}

.w_400 {
  width: 400px;
}

.m_auto {
  margin: auto;
}

.ml__auto {
  margin-left: auto;
}

```

```html
<p>Lorem ipsum</p>
<p class="w_400">Lorem ipsum</p>
<p class="w_400 m_auto">Lorem ipsum</p>
<p class="w_400 ml_auto">Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 5px solid #000;">Lorem ipsum</p>
  <p style="border: 5px solid #000; width: 400px;">Lorem ipsum</p>
  <p style="border: 5px solid #000; width: 400px; margin: auto;">Lorem ipsum</p>
  <p style="border: 5px solid #000; width: 400px; margin-left: auto;">Lorem ipsum</p>
</div>

## [Height](https://developer.mozilla.org/en-US/docs/Web/CSS/height)

> <b>Value:</b> [ `<length>` | `<percentage>` | auto ]

### Syntax

```css
/* <length> values */
height: 300px;
height: 25em;

/* <percentage> value */
height: 75%;
```

### Example

```css
p {
  border: 5px solid #000;
}

.h_50 {
  height: 50px;
}
```

```html
<p>Lorem ipsum</p>
<p></p>
<p class="w_400">Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 5px solid #000;">Lorem ipsum</p>
  <p style="border: 5px solid #000;"></p>
  <p style="border: 5px solid #000; height: 50px;">Lorem ipsum</p>
</div>

<!-- 
TODO

max-width

min-width

box-sizing
https://mdn.mozillademos.org/files/13649/box-model-alt-small.png
https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Box_model_recap

overflow

outline

[`border-colapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-colapse)


[`border-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image)

[`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

[`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) 

-->
