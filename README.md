# aframe-mss

> **Work in progress**

Mixin Style Sheets: CSS for A-Frame.

Declaratively declare mixins in a stylesheet form:

```css
/* example.mss */

wideBox {
  geometry {
    primitive: box;
    width: 5;
  }
}

red {
  material {
    color: #FF2222;
  }
}
```

Then import and use from A-Frame:

```html
<a-scene>
  <a-assets>
    <a-style src="example.mss"></a-style>
  </a-assets>

  <a-entity mixin="red wideBox"></a-entity>
</a-scene>
```
