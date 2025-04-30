# Border

The design properties for the border component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **thickness** | number | 0 | The thickness of the border in mm. |
| **colour** | string\|array | 'black' | The border [colour](/other/colour.md). |
| **radius** | number | 3 | The radius of border's corners. |
| **innerMargin** | number | 5 | The minimum gap between border and inner plater content. |
| **innerColour** | string\|array\|null | null | The inner fill [colour](/other/colour.md) typically used for [metal plates](/examples/oblongs.md#metal-oblong). |

## Methods <!-- {docsify-ignore} -->

### setThickness()

Sets the border thickness in mm. It takes a *number*.

Returns: `Border`

### setColour()

Sets the border [colour](/other/colour.md). It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `Border`

### setRadius()

Sets the radius of the border's corners in mm. It takes a *number*.

Returns: `Border`

### setInnerMargin()

Sets the inner margin of the border in mm. It takes a *number*. It is the minimum gap between the stroke of the border and the beginning of the inner plate content (the registration and, if utilised, an inner side badge)

Returns: `Border`

### setInnerColour()

Optionally sets the border's inner [colour](/other/colour.md). It takes a *string* for a solid colour, or an *array* of strings for a gradient.

**Note:** Usually a number plate's border is a rectangular element with a stroke and no fill. However, this method allows you to fill it if you want to. It is useful when representing a [metal plate](/examples/oblongs.md#metal-oblong).

Returns: `Border`

### utilise()

Toggle the Border component on or off. It takes a *boolean*.

Returns: `Border`

### isUtilised()

Use to check if the Border component is being utilised or not.

Returns: `boolean`

### reset()

Removes (un-utilises) the Border component and resets its design properties to the defaults.

Returns: `Border`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised Border design properties.

Returns: `object`

### freshProperties()

Resets all Border design properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `Border`