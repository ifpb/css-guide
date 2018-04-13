# Box Model

## [Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

### Inline

```html
<span>Lorem ipsum</span>
<span>dolor</span>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <span>Lorem ipsum</span>
  <span>dolor</span>
</div>

### Block

```html
<p>Lorem ipsum</p>
<p>Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p>Lorem ipsum</p>
  <p>Lorem ipsum</p>
</div>

![Box Model](https://mdn.mozillademos.org/files/13647/box-model-standard-small.png)<br>
Fonte: [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Box_model_recap)

### Inline-block

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

```css
#first {
  border: 2px dotted #000;
}

#second, #last {
  border: 5px solid #000;
}
```

```html
<p id="first">Lorem ipsum</p>
<p id="second">Lorem ipsum</p>
<p id="last">Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 2px dotted #000;">Lorem ipsum</p>
  <p style="border: 5px solid #000;"></p>
  <p style="border: 5px solid #000;">Lorem ipsum</p>
</div>

**Margin**

```css
p {
  border: 5px dotted #000;
  margin: 3rem;
}
```

```html
<p>Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 5px solid #000; margin: 3rem;">Lorem ipsum</p>
</div>

## [Padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

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

## [Width](https://developer.mozilla.org/en-US/docs/Web/CSS/width) x [Height](https://developer.mozilla.org/en-US/docs/Web/CSS/height)

```css
p {
  border: 5px solid #000;
  padding: 3rem;
  width: 400px;
  height: 50px;
}
```

```html
<p>Lorem ipsum</p>
```

<div style="border-radius: 0.3rem;background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;">
  <p style="border: 5px solid #000; width: 400px; height: 50px;">Lorem ipsum</p>
</div>


<!-- ### Border

#### [`border-colapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-colapse)

#### [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color)

#### [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)

#### [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)

#### [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

#### [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) -->
