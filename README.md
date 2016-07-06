# aframe-mss

Mixin Style Sheets: CSS for [A-Frame][aframe].

<img alt="logo" src="mss.png" width="320">

## Usage

Declaratively declare [mixins][mixins] and [components][components] in a stylesheet form:

```css
/* example.mss */

red {
  material {
    color: #393E51;
  }
}

white {
  material {
    color: #E9E6C9;
  }
}

blue {
  material {
    color: #566683;
  }
}

box {
  geometry {
    primitive: box;
  }
}

sphere {
  geometry {
    primitive: sphere;
  }
}

sky {
  geometry {
    primitive: sphere;
    radius: 5000;
    segmentsHeight: 20;
    segmentsWidth: 64;
  }
  material {
    shader: flat;
  }
  scale: -1 1 1;
}

left { position: -1 0 0; }
right { position: 1 0 0; }
```

Then import using `<a-style>` and use via mixins:

```html
<a-scene>
  <a-assets>
    <a-style src="basic.mss"></a-style>
  </a-assets>

  <a-entity mixin="left red box"></a-entity>
  <a-entity mixin="right blue sphere"></a-entity>
  <a-entity mixin="white sky"></a-entity>
</a-scene>
```

[aframe]: https://aframe.io/
[components]: https://aframe.io/docs/0.2.0/core/component.html
[mixins]: https://aframe.io/docs/0.2.0/core/mixins.html
