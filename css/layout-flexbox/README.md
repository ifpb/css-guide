# CSS Flexible Box Layout Module (Flexbox)


## Flexbox Terminology
---

![](https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg)<br>
Reference: [W3C](https://www.w3.org/TR/css-flexbox-1/)

Terminology: 
* Flex container
* Flex item
* Main axis (main-start, main-end)
* Cross axis (cross-start, cross-end)

## Display
---

> <b>Value:</b> flex \| inline-flex

## Flex Container - Orientation Direction
---

> <b>Name:</b> flex-direction<br>
> <b>Value:</b> row \| row-reverse \| column \| column-reverse<br>
> <b>Initial:</b>	row

### Example

[directions/index.html](directions/index.html):
<iframe src="directions/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Container - Orientation Wrap
---
> <b>Name:</b> flex-wrap<br>
> <b>Value:</b> nowrap | wrap | wrap-reverse<br>
> <b>Initial:</b>	nowrap

### Example

[wraps/index.html](wraps/index.html):
<iframe src="wraps/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Container - Orientation Direction & Wrap
---

> <b>Name:</b> flex-flow<br>
> <b>Value:</b> `<flex-direction>` || `<flex-wrap>`<br>
> <b>Initial:</b>	individual properties

### Example

[directions-wraps/index.html](directions-wraps/index.html):
<iframe src="directions-wraps/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Container - Alignment Content (Justify)
---

> <b>Name:</b>	`justify-content`<br>
> <b>Value:</b> flex-start | flex-end | center | space-between | space-around<br>
> <b>Initial:</b> flex-start

### Example

[justify-contents/index.html](justify-contents/index.html):
<iframe src="justify-contents/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Container - Alignment Items
---

> <b>Name:</b>	`align-items`<br>
> <b>Value:</b> flex-start | flex-end | center | baseline | stretch<br>
> <b>Initial:</b> stretch

### Example

[alignment-items/index.html](alignment-items/index.html):
<iframe src="alignment-items/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Container - Alignment Content
---

> <b>Name:</b> `align-content`<br>
> <b>Value:</b> flex-start | flex-end | center | space-between | space-around | stretch<br>
> <b>Initial:</b> stretch

### Example

[alignment-content/index.html](alignment-content/index.html):
<iframe src="alignment-content/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Alignment Self
---

> <b>Name:</b> `align-self`<br>
> <b>Value:</b> auto | flex-start | flex-end | center | baseline | stretch<br>
> <b>Initial:</b> auto

### Example

[alignment-self/index.html](alignment-self/index.html):
<iframe src="alignment-self/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Ordering
---

> <b>Name:</b> `order`<br>
> <b>Value:</b> `<integer>`<br>
> <b>Initial:</b> 0<br>

### Example

[ordering/index.html](ordering/index.html):
<iframe src="ordering/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Flexibility Grow
---

> <b>Name:</b> `flex-grow`<br>
> <b>Value:</b> `<integer>`<br>
> <b>Initial:</b> 0<br>

### Example

[flexibility-grow/index.html](flexibility-grow/index.html):
<iframe src="flexibility-grow/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Flexibility Shrink
---

> <b>Name:</b> `flex-shrink`<br>
> <b>Value:</b> `<integer>`<br>
> <b>Initial:</b> 1<br>

### Example

[flexibility-shink/index.html](flexibility-shink/index.html):
<iframe src="flexibility-shink/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Flexibility Basis
---

> <b>Name:</b> flex-basis<br>
> <b>Value:</b> content | `<width>`<br>
> <b>Initial:</b> auto<br>

### Example

[flexibility-basis/index.html](flexibility-basis/index.html):
<iframe src="flexibility-basis/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Flex Item - Flexibility Shorthand
---

> <b>Name:</b> flex<br>
> <b>Value:</b> none | [ `<flex-grow>` `<flex-shrink>`? || `<flex-basis>` ]<br>
> <b>Initial:</b> 0 1 auto<br>

### Example

[flexibility/index.html](flexibility/index.html):
<iframe src="flexibility/index.html" style="width: 100%; border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Demo
---

[Cards](cards/) ([Article](https://codeburst.io/build-a-minimalist-html-card-in-just-53-lines-of-code-with-flexbox-b40801927eb5), [Source](https://github.com/bmorelli25/flexbox-card-tutorial)), [Holy Grail Layout](holy-grail-layout/), [Menu](menu/)

## References
---

* [CSS Flexible Box Layout Module Level 1 \| W3C](https://www.w3.org/TR/css-flexbox-1/)
* [Basic concepts of flexbox \| MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
* [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [Can I Use - CSS Flexible Box Layout Module](https://caniuse.com/#feat=flexbox)
* [Build a Minimalist HTML Card in just 53 lines of code (with Flexbox)](https://codeburst.io/build-a-minimalist-html-card-in-just-53-lines-of-code-with-flexbox-b40801927eb5)
* [How Flexbox works — explained with big, colorful, animated gifs](https://medium.freecodecamp.org/an-animated-guide-to-flexbox-d280cf6afc35)
* [Learn CSS Flexbox in 5 Minutes](https://medium.freecodecamp.org/learn-css-flexbox-in-5-minutes-b941f0affc34)
* [Flexbox Cheat Sheet](https://yoksel.github.io/flex-cheatsheet/)
* [Flexbox - A friendly tutorial for modern CSS layouts](https://internetingishard.com/html-and-css/flexbox/)
* [Flexbox - Use Flexbox para levar a criação de layouts CSS ao próximo nível](http://desenvolvimentoparaweb.com/css/flexbox/)
* [Guia Flexbox](https://origamid.com/projetos/flexbox-guia-completo/)

<script>
  const iframes = Array.from(document.querySelectorAll('iframe'))
  for (const iframe of iframes) {
    const height = parseInt(iframe.contentDocument.body.offsetHeight) + 32
    iframe.style.height = `${height}px`
  }
</script>