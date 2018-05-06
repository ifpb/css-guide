# [Media Queries](https://docs.webplatform.org/wiki/css/mediaqueries)

* [Syntax](#syntax)
* [Examples](#examples)
* [Responsive Design](#responsive-design)

## Syntax
---

* [Media types](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_types): `all`, `print`, `screen`, `speech`
* [Media features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features): `width`, `height`, `orientation`
* [Logical operators](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Logical_operators): `and`, `not`, `only`

## Examples
---

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

## Responsive Design
---

```css
/* rulesets */

@media screen and (min-width: 500px) {
  /* rulesets */
}

@media screen and (min-width: 1000px) {
  /* rulesets */
}
```

## References
---

* Doc: [WP](https://docs.webplatform.org/wiki/css/mediaqueries), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index) e [W3C](https://www.w3.org/TR/2012/REC-css3-mediaqueries-20120619/)
* [A Guide To The State Of Print Stylesheets In 2018](https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/)
