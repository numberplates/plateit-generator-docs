# Importing & Exporting

> Note: the term "export" is being used on this page, but it's referring to "getting" data as opposed to actually exporting a file.

## Objects

It is possible to import and export plate designs using JSON/JavaScript objects. This is useful if you want to continue editing a plate at a later time.

A practical use for imports is to render on-the-fly previews with a single design object (no need to use the public methods for each individual component).

### Export Plate

Let's say you have finished creating a plate. You can grab the object representation of it by calling:

```javascript
plate.file.exportObject()
```

Optional argument:

* `incDataUrls` (*boolean*, default: `true`) — include side badge cover image data URLs. Pass `false` to use SVG image references instead. See [Side Badge Covers](side-badge-covers.md).

It will return an object resembling something similar to the following:

```javascript
{
  "document": {
    "width": 520,
    "height": 111,
    "margin": 5
  },
  "background": {
    "backgroundColour": "yellow",
    "doNotPrint": true
  },
  "reg": {
    "text": "NG25 XYZ",
    "textFontSrc": "../assets/fonts/CharlesWright-Car.ttf",
    "textHeight": 79,
    "textLineGap": 19,
    "textColour": "black"
  },
  "bottomLine": {
    "text": "Acme Number Plates SW1A 2AA",
    "textFontSrc": "../assets/fonts/OpenSans-Regular.ttf",
    "textHeight": 4,
    "textColour": "black"
  },
  "bsau": {
    "text": "Acme BSAU 145e",
    "textFontSrc": "../assets/fonts/OpenSans-Regular.ttf",
    "textHeight": 3,
    "textColour": "black",
    "isInBorder": true
  },
  "meta": {
    "generator": "Plateit 4.0.0"
  }
}
```

### Import Plate

To import a plate design you can use the `importObject()` method.

It takes one argument:

* 1) *object* - The plate's design object (such as the example export above)

```javascript
plate.file.importObject(plateDesign)
```
> This will create a fresh plate, overwriting all existing design properties.

### Export Component

Each component has a `getProperties()` method which will return just that component's object. For example: `plate.border.getProperties()`.

It will return an object resembling the following:

```javascript
{
  "thickness": 2,
  "colour": "black",
  "radius": 3,
  "innerMargin": 5
}
```

### Import Component

Each component has a `freshProperties()` method which will reset all of its design properties to the defaults and overwrite them with any new ones passed to it. For example:

```javascript
plate.border.freshProperties({
  'thickness': 3,
  'colour': 'blue'
})
```

## SVGs

### Import Plate

Call `plate.file.importSvg()` to import an SVG plate file.

It takes one argument:

* 1) *string* - The plate's SVG string 

Use `await plate.file.importSvg(svgString)`. Cover image references are restored automatically; see [Side Badge Covers](side-badge-covers.md).

!> It is **only** possible to import an SVG if it has been exported using this application *with* design metadata embedded into it (see below). Importing an SVG file with no supporting metadata will not work!

### Export Plate

Call `plate.file.exportSvg()` to return the finished number plate's SVG string.

It takes one argument:

* `incMetadata` (*boolean*, default: `false`) — embed the design object as JSON metadata, using references for cover image data URLs. See [Side Badge Covers](side-badge-covers.md).

SVGs with embedded design metadata can be brought back into the application for further editing as explained above.

With metadata enabled, the returned SVG string will look something like this:

```xml
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.dev/svgjs" generator="Plateit 4.0.0" viewBox="0 0 520 111" preserveAspectRatio="xMidYMid meet">
  <metadata>
    <design xmlns="urn:plateit:design:1">
      <!-- json object embedded here -->
    </design>
  </metadata>
  <!-- remaining SVG data here -->
</svg>
```

The exported SVG data can now be passed to the Plateit server-side API along with any additional order information. Instructions will be provided in the [separate API documentation](https://numberplates.github.io/plateit-api-docs).
