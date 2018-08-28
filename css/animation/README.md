# [Animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)

## Syntax
---

> <b>Value:</b> `<time>` \|\| `<single-timing-function>` \|\| `<time>` \|\| `<single-animation-iteration-count>` \|\| `<single-animation-direction>` \|\| `<single-animation-fill-mode>` \|\| `<single-animation-play-state>` \|\| [ none \| `<keyframes-name>` ]

```css
/* @keyframes duration | timing-function | delay | 
iteration-count | direction | fill-mode | play-state | name */
animation: 3s ease-in 1s 2 reverse both paused slidein;

/* @keyframes duration | timing-function | delay | name */
animation: 3s linear 1s slidein;

/* @keyframes duration | name */
animation: 3s slidein;
```

## Spinner
---

```css
.spinner {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: 5px solid #ccc;
  border-right-color: #000;
  animation: spinner 1s linear infinite;
}

@keyframes spinner {
  to {
    transform: rotate(360deg);
  }
}
```

[spinner/index.html](spinner/index.html):

<iframe 
  src="spinner/index.html" 
  width="100%"
  height="300px"
  frameborder="0"
  allowfullscreen>
</iframe>

## Bounce
---

```css
@keyframes bounce {
  from,
  20%,
  53%,
  80%,
  to {
    transform: translateY(0);
    animation-timing-function: ease-in;
  }
  40% {
    transform: translateY(-100px);
    animation-timing-function: ease-out;
  }
  70% {
    transform: translateY(-50px);
    animation-timing-function: ease-out;
  }
  90% {
    transform: translateY(-50px);
  }
}

.bounce {
  animation-name: bounce;
  animation-duration: 2s;
  animation-delay: .5s;
}
```

[bounce/index.html](bounce/index.html):

<iframe 
  src="bounce/index.html" 
  width="100%"
  height="300px"
  frameborder="0"
  allowfullscreen>
</iframe>

## References
---

- [CSS Animations - Guia de bolso](https://legacy.gitbook.com/book/daliannyvieira/css-animations-pocket-guide/details)
- [Using CSS animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- [CSS Animations Level 1](https://www.w3.org/TR/css-animations-1/)
- [Keyframe Animation Syntax](https://css-tricks.com/snippets/css/keyframe-animation-syntax/)
- [@keyframes](https://tympanus.net/codrops/css_reference/keyframes/)
- [Create 2-state, SVG-powered animated icons (Icon Transition Generator)](https://blog.nucleoapp.com/create-2-state-svg-powered-animated-icons-76ed19160a7e)
- Library
  - [The Top 9 Animation Libraries for UI Designers in 2017](https://www.sitepoint.com/our-top-9-animation-libraries/)
  - [Animate.css](https://daneden.github.io/animate.css/)
  - [Hover.css - A collection of CSS3 powered hover effects](http://ianlunn.github.io/Hover/)
  - [Animista](http://animista.net/play/basic/slide-fwd)
- CSS Animations 
  - [Pure CSS Loaders](https://loading.io/css/)
  - [16 top CSS animation examples](https://www.creativebloq.com/inspiration/css-animation-examples)
  - [15 New Awesome Creative CSS Animations](https://cssnewbie.com/15-new-awesome-creative-css-animations/#.W049pS2ZM0o)
  - [30 Cool CSS Animations You Have To See](https://www.hongkiat.com/blog/creative-css-animations/)
  - [20 Best CSS Animations on CodeCanyon](https://code.tutsplus.com/tutorials/20-best-css-animations--cms-27561)
