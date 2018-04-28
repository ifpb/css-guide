# [Properties](https://docs.webplatform.org/wiki/css/properties)

* [Properties](#properties)
* [Shorthand Properties](#shorthand-properties)
* [Values and Units](#values-and-units)

## Properties
---

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

## Shorthand Properties
---

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

## Other Properties
---

* [Typography](typography.html)
* [Web Font](web-font.html)
* [Icons](icon.html)
* [Hyperlinks](links.html)
* [Box model](box-model.html)
* [Background](background.html)


## Values and Units
---

### [`<length>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length)

#### absolute units

```css
p {
  font-size: 17px;
}
```

#### relative units

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

### [`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

```css
h1 {
  color: red;
}

p {
  color: rgb(255, 0, 0);
}
```

## References
---

* Properties:
  * Doc: [WP](https://docs.webplatform.org/wiki/css/properties), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/CSS2/propidx.html)<br>
  * Cheat Sheet: [smashing](https://www.smashingmagazine.com/2009/07/css-3-cheat-sheet-pdf/) ([pdf](https://www.smashingmagazine.com/wp-content/uploads/images/css3-cheat-sheet/css3-cheat-sheet.pdf)), [w3school](http://www.w3schools.com/cssref/), [tutorialspoint](http://www.tutorialspoint.com/css/css_references.htm), [1stwebdesigner](http://www.1stwebdesigner.com/freebies/css-cheat-sheets-designers/)
* Color
  * [Color Table](values.md#color)
  * [CSS values and units \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Values_and_units) (Numeric values, Percentages, Colors, Coordinate positions, Functions)
* [Value definition syntax \| MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Value_definition_syntax)