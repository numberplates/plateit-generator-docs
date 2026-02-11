# Colour

Colours can be set using a *string* or an *array* of strings, depending on whether you want a solid colour or a gradient.

## Solid Colours

For a component to render a solid colour, simply pass a *string* with a valid colour hex code, or a universally recognised css colour name. For example: `'black'` or `'#000000'`.

## Opacity

Opacity can be adjusted within the same string by appending an `@` sign followed by the opacity value (a number between 0 and 1). For example: `'green@0.5'`

## Gradients

For a component to render a gradient, you can pass an *array* of strings following the same rules as above. By default, the gradient will be *linear* and will render from *left to right*.

To control the type of gradient, add a final string to the array consisting of one of the following characters:

`x` - Renders a *linear* gradient from left to right (this is the default)

`y` - Renders a *linear* gradient from top to bottom

`r` - Renders a *radial* gradient from inside to outside

To reverse a gradient, define the colour values in the opposite order.

## Examples

### Solid Colours <!-- {docsify-ignore} -->

```javascript
// Set a blue side badge with a css-recognised colour name.
plate.sideBadgeLeft.setBackgroundColour('blue')

// Set a blue side badge with a colour hex code.
plate.sideBadgeLeft.setBackgroundColour('#0000ff')

// Set a blue side badge with a colour hex code and lower its opacity.
plate.sideBadgeLeft.setBackgroundColour('#0000ff@0.5')
```

### Gradients <!-- {docsify-ignore} -->

```javascript
// A left-to-right, blue-to-red gradient using css colour names.
plate.sideBadgeLeft.setBackgroundColour(['blue', 'red'])

// A left-to-right, blue-to-red gradient using colour hex codes.
plate.sideBadgeLeft.setBackgroundColour(['#0000ff', '#ff0000'])

// A top-to-bottom, blue-to-red gradient.
plate.sideBadgeLeft.setBackgroundColour(['blue', 'red', 'y'])

// A radial, blue-to-red gradient.
plate.sideBadgeLeft.setBackgroundColour(['blue', 'red', 'r'])

// A top-to-bottom, blue-to-red-to-yellow gradient.
plate.sideBadgeLeft.setBackgroundColour(['blue', 'red', 'yellow', 'y'])

// A top-to-bottom, blue-to-red gradient with differing opacities.
plate.sideBadgeLeft.setBackgroundColour(['blue@0.5', 'red', 'y'])

```