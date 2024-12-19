# Setup

>This page assumes you have followed the initial [installation instructions](installation.md).

## Create an HTML Container

On the html page/s you want to include the number plate design functionality, define an empty `<div>` tag with a unique id. This will become the container for your preview image.

```html
<div id="number-plate-preview"></div>
```

## Instantiate the Plate Class

Inside your own custom JavaScript file, instantiate the `Plate` class under a variable name of your choosing (a logical variable name is `plate`, or `frontPlate`, or `rearPlate`). In the class constructor, you need to pass your container's ID selector. For example:

```javascript
const plate = new Plate('#number-plate-preview')
```

> Note: if referencing the "IIFE" script in the header or footer of an html page, you'll need to invoke the class slightly differently:

```javascript
const plate = new Plateit.Plate('#number-plate-preview')
```

> Note: if running the application [on a server](server.md), invoke the class *without* an ID selector.

## Manipulate the Plate

You can now manipulate your number plate in the following manner:

```javascript
plate.document.setWidth(520)
plate.document.setHeight(111)
plate.reg.setText('MY REG')
// etc... etc...
```

You can learn more about this in the [next section](objects.md).

## External Asset Caching

For front-end applications, typically there will be more than one Plate instantiated at a time to render both a front and rear plate simultaneously. To help with asset caching (and to avoid having to fetch the same asset twice), you can instantiate the Plate class with an optional asset helper like so:

```javascript
const assetsFetched = new AssetsFetched()
const plateFront = new Plate('#front-plate-preview', assetsFetched)
const rearFront = new Plate('#rear-plate-preview', assetsFetched)
```