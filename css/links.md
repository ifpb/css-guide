# Styling Hyperlinks

References:
- [Styling Hyperlinks \| W3C](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links)

## Link States

| State | Selector | Style | Preview |
|-|-|-|-|
| Unvisited | :link | color: rgb(0, 0, 238); | <a href="#" style="text-decoration: underline; cursor: pointer; color: rgb(0, 0, 238);">link</a> |
| Visited | :visited | color: rgb(85, 26, 139); | <a href="#" style="text-decoration: underline; cursor: auto; color: rgb(85, 26, 139);">link</a> |
| Hover | :hover | cursor: pointer; | <a href="#" style="text-decoration: underline; cursor: auto; color: rgb(85, 26, 139);">link</a> |
| Focus | :focus | outline: rgb(59, 153, 252) auto 5px; | <a href="#" style="text-decoration: underline; cursor: auto; color: rgb(0, 0, 238); outline: rgb(59, 153, 252) auto 5px;">link</a> |
| Active | :active | color: rgb(238, 0, 0); | <a href="#" style="text-decoration: underline; cursor: auto; color: rgb(238, 0, 0);">link</a> |

Properties: [color](https://developer.mozilla.org/en-US/docs/Web/CSS/color), [cursor](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor), [outline](https://developer.mozilla.org/en-US/docs/Web/CSS/outline), [text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

[link/index.html](link/index.html):
```css
a {
  outline: none;
  text-decoration: none;
}


a:link {
  color: blue;
}

a:visited {
  color: purple;
}

a:active {
  color: red;
}

a:hover, a:active, a:focus {
  text-decoration: underline;
}
```
