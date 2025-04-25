# Document

The design properties for the document component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **width** | number | 520 | The width of the document (plate) in mm. |
| **height** | number | 111 | The height of the document (plate) in mm. |
| **margin** | number | 5 | The print margin in mm. |

## Methods <!-- {docsify-ignore} -->

### setWidth()

Sets the plate width in mm. It takes a *number*.

Returns: `Document`

### setHeight()

Sets the plate height in mm. It takes a *number*.

Returns: `Document`

### setMargin()

Sets the margin (spacing round the outside) in mm. It takes a *number*.

Returns: `Document`

### render()

Renders the Document (plate size) component only. All other components will be left un-rendered. It's recommended to use the [plate.render()](/rendering.md) method instead after changes have been made to the Document properties.

Returns: `Promise`

### reset()

Resets the Document properties to the defaults.

Returns: `Document`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised Document properties.

Returns: `object`

### freshProperties()

Resets the Document properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `Document`