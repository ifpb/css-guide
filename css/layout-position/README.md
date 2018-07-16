# Position CSS

## Static positioning
---

[demo/static.html](demo/static.html):

```css
#two {
  background-color: #eee;
  position: static;
}
```

<iframe 
  src="demo/static.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

## Relative positioning
---

### top, bottom, left, and right

[demo/relative.html](demo/relative.html):

```css
#two {
  background-color: #eee;
  position: relative;
  top: 5.8vw;
  left: 5.8vw;
}
```

<iframe 
  src="demo/relative.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

### z-index

[demo/z-index.html](demo/z-index.html):

```css
#two {
  background-color: #eee;
  position: relative;
  top: 5.8vw;
  left: 5.8vw;
  z-index: -1;
}

#three {
  z-index: -2;
}
```

<iframe 
  src="demo/z-index.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

## Absolute positioning
---

[demo/absolute.html](demo/absolute.html):

```css
#two {
  background-color: #eee;
  position: absolute;
  top: 5.8vw;
  left: 5.8vw;
}
```

<iframe 
  src="demo/absolute.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

### Positioning contexts

[demo/static-absolute.html](demo/static-absolute.html):

```html
<div class="static parent">
  <div class="absolute child"></div>
</div>
```

```css
.static {
  position: static;
}

.absolute {
  position: absolute;
  top: 20px;
  left: 20px;
}
```

<iframe 
  src="demo/static-absolute.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

[demo/rel-absolute.html](demo/rel-absolute.html):

```html
<div class="relative parent">
  <div class="absolute child"></div>
</div>
```

```css
.relative {
  position: relative;
  top: 20px;
  left: 20px;
}

.absolute {
  position: absolute;
  top: 20px;
  left: 20px;
}
```

<iframe 
  src="demo/rel-absolute.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

[demo/rel-rel-absolute.html](demo/rel-rel-absolute.html):

```html
<div class="relative grandparent">
  <div class="relative parent">
    <div class="absolute child"></div>
  </div>
</div>
```

```css
.relative {
  position: relative;
  top: 20px;
  left: 20px;
}

.absolute {
  position: absolute;
  top: 20px;
  left: 20px;
}
```

<iframe 
  src="demo/rel-rel-absolute.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

## Fixed positioning
---

[demo/fixed.html](demo/fixed.html):

```css
#two {
  background-color: #eee;
  position: fixed;
  top: 5.8vw;
  left: 5.8vw;
}
```

<iframe 
  src="demo/fixed.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

## Sticky positioning
---

[demo/sticky.html](demo/sticky.html):

```css
dt {
    position: -webkit-sticky;
    position: sticky;
    top: -1px;
  }
```

<iframe 
  src="demo/sticky.html" 
  style="border-radius: 0.3rem; border: solid 1px #dce6f0; padding: 0.8rem;"
  width="100%"
  height="300"
  frameborder="0"
  allowfullscreen>
</iframe>

## References
---

- [How browsers position floats – Monica Dinculescu](https://meowni.ca/posts/float-layout/)
- Position
  - Propriedades: `position`, `top`, `left`, `right`, `bottom`, `z-index`, `float`, `clear`, `display`
  - Position values: `static` \| `relative` \| `absolute` \| `sticky` \| `fixed`
    - [static](../codes/css/layout/position/static.html)
    - [relative](../codes/css/layout/position/relative.html)
    - [absolute](../codes/css/layout/position/absolute.html)
      - *Closest positioned*: [relative > absolute](../codes/css/layout/position/rel-absolute.html), [relative > relative > absolute](../codes/css/layout/position/rel-rel-absolute.html), [static > absolute](../codes/css/layout/position/static-absolute.html)
      - Altura do container: [relative > absolute](../codes/css/layout/position/rel-absolute-parentHeigth.html), [static > static](../codes/css/layout/position/static-static-parentHeight.html)
    - [fixed](../codes/css/layout/position/fixed.html)
    - [sticky](../codes/css/layout/position/sticky.html)
  - Sobreposição (`z-index`)
  - Reference: [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position), [CSS Tricks](https://css-tricks.com/almanac/properties/p/position/)
  - Exemplos: [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position#Examples), [Learn CSS Layout](http://learnlayout.com/position.html)
  - [All About Floats - CSS Tricks](https://css-tricks.com/all-about-floats/)
  - [5 Things You Might Not Know About the CSS Positioning Types](https://scotch.io/bar-talk/5-things-you-might-not-know-about-the-css-positioning-types)