# Position CSS

## Static positioning
---

```css
#two {
  background-color: #eee;
  position: static;
}
```

<iframe 
  src="demo/static.html" 
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
  allowfullscreen>
</iframe>

## Relative positioning
---

### top, bottom, left, and right

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
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
  allowfullscreen>
</iframe>

### z-index

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
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
  allowfullscreen>
</iframe>

## Absolute positioning
---

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
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
  allowfullscreen>
</iframe>

## Fixed positioning
---

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
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
  allowfullscreen>
</iframe>

## Sticky positioning
---

```css
dt {
    position: -webkit-sticky;
    position: sticky;
    top: -1px;
  }
```

<iframe 
  src="demo/sticky.html" 
  width="600"
  height="600"
  frameborder="0"
  style="border:0" 
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