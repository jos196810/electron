# View

> A View.

Process: [Main](../glossary.md#main-process)

This module cannot be used until the `ready` event of the `app`
module is emitted.

```javascript
// TODO example
```

## Class: View

> A View.

Process: [Main](../glossary.md#main-process)

`View` is an [EventEmitter][event-emitter].

### `new View()`

Creates a new `View`.

### Instance Methods

Objects created with `new View` have the following instance methods:

#### `view.addChildView(view)`

* `view` View - child view to add.

#### `view.removeChildView(view)`

* `view` View - child view to remove.

#### `view.setBounds(bounds)`

* `bounds` [Rectangle](structures/rectangle.md) - new bounds of the View.

#### `view.getBounds()`

Returns [`Rectangle`](structures/rectangle.md) - the bounds of this View, relative to its parent.

#### `view.setBackgroundColor(color)`

* `color` string - Color in Hex, RGB, ARGB, HSL, HSLA or named CSS color format. The alpha channel is
  optional for the hex type.

Examples of valid `color` values:

* Hex
  * `#fff` (RGB)
  * `#ffff` (ARGB)
  * `#ffffff` (RRGGBB)
  * `#ffffffff` (AARRGGBB)
* RGB
  * `rgb\(([\d]+),\s*([\d]+),\s*([\d]+)\)`
    * e.g. `rgb(255, 255, 255)`
* RGBA
  * `rgba\(([\d]+),\s*([\d]+),\s*([\d]+),\s*([\d.]+)\)`
    * e.g. `rgba(255, 255, 255, 1.0)`
* HSL
  * `hsl\((-?[\d.]+),\s*([\d.]+)%,\s*([\d.]+)%\)`
    * e.g. `hsl(200, 20%, 50%)`
* HSLA
  * `hsla\((-?[\d.]+),\s*([\d.]+)%,\s*([\d.]+)%,\s*([\d.]+)\)`
    * e.g. `hsla(200, 20%, 50%, 0.5)`
* Color name
  * Options are listed in [SkParseColor.cpp](https://source.chromium.org/chromium/chromium/src/+/main:third_party/skia/src/utils/SkParseColor.cpp;l=11-152;drc=eea4bf52cb0d55e2a39c828b017c80a5ee054148)
  * Similar to CSS Color Module Level 3 keywords, but case-sensitive.
    * e.g. `blueviolet` or `red`

**Note:** Hex format with alpha takes `AARRGGBB` or `ARGB`, _not_ `RRGGBBA` or `RGA`.

### Instance Properties

Objects created with `new View` have the following properties:

#### `view.children` _Readonly_

A `View[]` property representing the child views of this view.