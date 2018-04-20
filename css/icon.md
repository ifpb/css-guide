# Icons

## References

- Image Icon (Raster, Vector):
  - [Flat Icon](https://www.flaticon.com) (png, svg, eps, psd, base 64)
  - [Share Icon](https://www.shareicon.net)
  - [Material Design Icons](https://materialdesignicons.com)
- Font Icon:
  - [Font Static](http://fontastic.me)
  - [Material Icons](https://material.io/icons/)
  - [Font Awesome](http://fontawesome.io)
  - [Glyphicons](http://glyphicons.com/)
  - [Octicons](https://octicons.github.com/)
  - [Nerd Font](https://nerdfonts.com)
  - [Weather Icon](https://erikflowers.github.io/weather-icons/)
  - [Skycons](https://darkskyapp.github.io/skycons/)

## [Flat Icon Image](https://www.flaticon.com)
---

[icon/flat-icon/](icon/flat-icon/):
```
site
├── css
│   └── master.css
├── img
│   ├── facebook.svg
│   ├── instagram.svg
│   └── twitter.svg
└── index.html
```

```css
ul {
  list-style-type: none;
}

li  {
  display: inline;
}

li img {
  width: 50px;
}
```

```html
<ul>
  <li>
    <a href="#">
      <img src="img/facebook.svg" alt="Logo Facebook">
    </a>
  </li>
  <li>
    <a href="#">
      <img src="img/instagram.svg" alt="Logo Instagram">
    </a>
  </li>
  <li>
    <a href="#">
      <img src="img/twitter.svg" alt="Logo Twitter">
    </a>
  </li>
</ul>
```

Output:

<iframe src="icon/flat-icon/" width="100%" style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## [Font Awesome](https://fontawesome.com/)
---

References:
- [Icon Gallery](https://fontawesome.com/icons?d=gallery)
- [Facebook Logo](https://fontawesome.com/icons/facebook-square?style=brands)

[icon/font-awesome/](icon/font-awesome/):
```
site
├── css
│   └── master.css
└── index.html
```

```css
a {
  font-size: 2rem;
  color: #3b5898;
  text-decoration: none;
}
```

```html
<a href="#">
  <i class="fab fa-facebook"></i>
</a>
```

Output:

<iframe src="icon/font-awesome/" width="100%" style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>

## Google [Material Icon]((https://material.io/icons/))
---

References:
- [Icon Gallery](https://material.io/icons/#itempool)

[icon/material-icon/](icon/material-icon/):
```
site
├── css
│   └── master.css
└── index.html
```

```css
a {
  text-decoration: none;
}

.material-icons {
  color: #ccc;
  font-size: 3rem;
}

.material-icons:hover {
  color: #000;
}
```

```html
<a href="#">
  <i class="material-icons">school</i>
</a>
```

Output:

<iframe src="icon/material-icon/" width="100%" style="border-radius: 0.3rem; background-color: #f3f6fa;border: solid 1px #dce6f0; padding: 0.8rem;"></iframe>
