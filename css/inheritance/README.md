# [Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)

[examples/index.html](examples/index.html):
```css
body {
  color: green;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: green;">Lorem ipsum</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: green;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</div>

[examples/not-inheritance.html](examples/not-inheritance.html):
```css
body {
  color: green;
}
h1 {
  color: red;
}
```

```html
<body>
  <h1>Lorem ipsum</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p>Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</body>
```

Output:

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <h1 style="color: red;">Lorem ipsum</h1>
  <p style="color: green;">Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
  <p style="color: green;">Eveniet amet laudantium aperiam nisi ratione at, blanditiis...</p>
</div>

## References
---

* [Inheritance \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)
* [CSS 2.2 Specification - Appendix F. Full property table (Inherited?)](https://www.w3.org/TR/CSS22/propidx.html)