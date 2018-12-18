# Design Responsive

* [Viewport](#viewport)
* [CSS Media query](#css-media-query)
* [Mobile First and Breakpoints](#mobile-first-and-breakpoints)
* [Responsive Image](#responsive-image)
* [Demo](#demo)

## Viewport
---

[Set the viewport](https://developers.google.com/web/fundamentals/design-and-ux/responsive/#set-the-viewport):
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

[Compare devices](https://www.mydevice.io)

## [CSS Media query](https://ifpb.github.io/css-guide/css/media-query/)
---

* [Media types](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_types): `all`, `print`, `screen`, `speech`
* [Media features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features): `width`, `height`, `orientation`
* [Logical operators](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Logical_operators): `and`, `not`, `only`

## Mobile First and Breakpoints
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

[menu/index.html](menu/index.html):
```css
ul {
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

@media screen and (min-width: 700px) {
  ul {
    flex-direction: row;
    justify-content: space-around;
  }
}

@media screen and (min-width: 1000px) {
  ul {
    justify-content: flex-end;
  }
}
```

## Responsive Image
---

[image-responsive/index.html](image-responsive/index.html):
```html
{% include_relative image-responsive/index.html %}
```

## Demo
---

- [Portfólio](portfolio/)
- [Holy Grail Layout](holy-grail-layout/)
- [Responsive Table](table-responsive/index.html)
- [Weather](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/weather-2.html) ([Responsive Web Design Basics \| Google](https://developers.google.com/web/fundamentals/design-and-ux/responsive/))
- [Responsive Web Design - Examples](https://responsivedesign.is/examples/)
- [Common Responsive Layouts with CSS Grid (and some without!)](https://medium.com/samsung-internet-dev/common-responsive-layouts-with-css-grid-and-some-without-245a862f48df)

## References
---

* [Responsive Web Design Basics \| Google](https://developers.google.com/web/fundamentals/design-and-ux/responsive/)
* [Your First Multi-Device Site \| Google](https://developers.google.com/web/fundamentals/codelabs/your-first-multi-screen-site/)
* [Responsive Web Design Fundamentals \| Google](https://udacity.com/course/responsive-web-design-fundamentals--ud893)
* [Responsive layout grid \| Material Design](https://material.io/design/layout/responsive-layout-grid.html)
* [Web para dispositivos móveis \| Caelum](https://www.caelum.com.br/apostila-html-css-javascript/web-para-dispositivos-moveis/): [CSS media types](https://www.caelum.com.br/apostila-html-css-javascript/web-para-dispositivos-moveis/#css-media-types), [CSS media queries](https://www.caelum.com.br/apostila-html-css-javascript/web-para-dispositivos-moveis/#css3-media-queries),  [Vieport](https://www.caelum.com.br/apostila-html-css-javascript/web-para-dispositivos-moveis/#viewport)
* [How to create a fully responsive navbar with Flexbox](https://medium.freecodecamp.org/how-to-create-a-fully-responsive-navbar-with-flexbox-a4435d175dd3)
* [Using Media Queries For Responsive Design In 2018](https://www.smashingmagazine.com/2018/02/media-queries-responsive-design-2018/?utm_campaign=CSS%2BLayout%2BNews&utm_medium=email&utm_source=CSS_Layout_News_132)