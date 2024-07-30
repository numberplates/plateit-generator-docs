# Setup

>This page assumes you have followed the initial [installation instructions](installation.md).

## Create an HTML Container

On the html page/s you want to include the number plate design functionality, define an empty `<div>` tag with a unique id. This will become the container for your preview image.

```html
<div id="number-plate-preview"></div>
```

## Instantiate the Plate Class

Inside your own custom javascript file, instantiate the `Plate` class under a variable name of your choosing (a logical variable name is `plate`, or `frontPlate`, or `rearPlate`). In the class constructor, you need to pass your container's ID selector. For example:

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