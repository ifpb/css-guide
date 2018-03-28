# CSS values and units

Reference:
* [CSS values and units \| MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Values_and_units) (Numeric values, Percentages, Colors, Coordinate positions, Functions)
* [Value definition syntax \| MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Value_definition_syntax)

<!-- TODO
Actual value
Computed value
Initial value
Resolved value
Specified value
Used value -->

## [`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
---

**[Color Keyword](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#Color_keywords)**

```css
/* <named-color> values */
color: white;
color: black;
color: red;
color: green;
color: blue;
color: cyan;
color: rebeccapurple;

/* <hex-color> values */
color: #ffffff;
color: #000000;
color: #ff0000;
color: #00ff00;
color: #0000ff;
color: #00ffff;
color: #663399;
color: #639;
color: #66339977;
color: #6397;

/* <rgb()> values */
color: rgb(255, 255, 255)
color: rgb(0, 0, 0)
color: rgb(255, 0, 0)
color: rgb(0, 255, 0)
color: rgb(0, 0, 255)
color: rgb(0, 255, 255)
color: rgb(102, 51, 153)
color: rgba(102, 51, 153, 0.5);

/* <hsl()> values */
color: hsl(0, 0%, 100%);
color: hsl(0, 0%, 0%);
color: hsl(0, 100%, 50%);
color: hsl(120, 100%, 50%);
color: hsl(240, 100%, 50%);
color: hsl(180, 100%, 50%);
color: hsl(270, 50%, 40%);
color: hsla(270, 50%, 40%, 0.5);
```

| &lt;named-color&gt; values | &lt;hex-color> values<br>(#rrggbb & [#rrggbbaa](https://caniuse.com/#feat=css-rrggbbaa)) | &lt;rgb()> values | [&lt;hsl()> values](https://en.wikipedia.org/wiki/HSL_and_HSV) |
|-|-|-|-|
| <span style="color: white">white</span> | <span style="color: #ffffff">#ffffff</span> | <span style="color: rgb(255, 255, 255)">rgb(255, 0, 0)</span> | <span style="color: hsl(0, 0%, 100%)"> hsl(0, 0%, 100%)</span> |
| <span style="color: black">black</span> | <span style="color: #000000">#000000</span> | <span style="color: rgb(0, 0, 0)">rgb(0, 0, 0)</span> | <span style="color: hsl(0, 0%, 0%)"> hsl(0, 0%, 0%)</span> |
| <span style="color: red">red</span> | <span style="color: #ff0000">#ff0000</span> | <span style="color: rgb(255, 0, 0)">rgb(255, 0, 0)</span> | <span style="color: hsl(0, 100%, 50%)"> hsl(0, 100%, 50%)</span> |
| <span style="color: green">green</span> | <span style="color: #00ff00">#00ff00</span> | <span style="color: rgb(0, 255, 0)">rgb(0, 255, 0)</span> | <span style="color: hsl(120, 100%, 50%)"> hsl(120, 100%, 50%)</span> |
| <span style="color: blue">blue</span> | <span style="color: #0000ff">#0000ff</span> | <span style="color: rgb(0, 0, 255)">rgb(0, 0, 255)</span> | <span style="color: hsl(240, 100%, 50%)"> hsl(240, 100%, 50%)</span> |
| <span style="color: cyan">cyan</span> | <span style="color: #00ffff">#00ffff</span> | <span style="color: rgb(0, 255, 255)">rgb(0, 255, 255)</span> | <span style="color: hsl(180, 100%, 50%)"> hsl(180, 100%, 50%)</span> |
| <span style="color: rebeccapurple">rebeccapurple</span> | <span style="color: #663399">#663399</span> <span style="color: #639">#639</span> | <span style="color: rgb(102, 51, 153)">rgb(102, 51, 153)</span><br><span style="color: rgba(102, 51, 153, 1)">rgba(102, 51, 153, 1)</span> | <span style="color: hsl(270, 50%, 40%)"> hsl(270, 50%, 40%)</span><br><span style="color: hsla(270, 50%, 40%, 1)"> hsla(270, 50%, 40%, 1)</span> |
| <span style="color: rgba(102, 51, 153, 0.5)">rebeccapurple 50%</span> | <span style="color: #66339977">#66339977</span> <span style="color: #6397">#6397</span> | <span style="color: rgba(102, 51, 153, 0.5)">rgba(102, 51, 153, 0.5)</span> | <span style="color: hsla(270, 50%, 40%, 0.5)"> hsla(270, 50%, 40%, 0.5)</span> |

**Tools**
- [Chrome DevTools: Color Picker](https://developers.google.com/web/tools/chrome-devtools/css/reference#color-picker)
- Color Info
  - Tools
    - [rgbTo](http://rgb.to/)
    - [color-hex](http://www.color-hex.com/)
    - [colourco](http://www.colourco.de/)
    - Google Search
  - Rebecca Purple Info (#663399):
    - [color-hex](http://www.color-hex.com/color/663399) (Shades, Tints, Triadic Colors, Analogous Colors, Monochromatic Colors, Complementary Color, Related Colors)
    - [rgbTo](http://rgb.to/rgb/102,51,153)

**[Color Model](https://en.wikipedia.org/wiki/Color_model)**
- [RGB](https://en.wikipedia.org/wiki/RGB_color_model) (additive color model)
- [CMYK](https://en.wikipedia.org/wiki/CMYK_color_model) (subtractive color model)

**Pastel Color**

## [`<length>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length)
---