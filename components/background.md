# Background

The design properties for the background component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **backgroundColour** | string\|array | 'none' | The [colour](/other/colour.md) of the background. |
| **shapeSrc** | string\|null | null | The path or url to a [shape template](/other/shaped-plates.md). |
| **doNotPrint** | boolean | true | If true, the background is for preview purposes only and will not be printed. |

## Methods <!-- {docsify-ignore} -->

### setBackgroundColour()

Sets the [colour](/other/colour.md) of the preview background. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `Background`

### setShape()

Sets the [shape template](/other/shaped-plates.md) for a shaped plate. It takes a *string* consisting of a relative path to the template file, or a fully formed URL. If you want to remove an existing shape, pass *null*.

Returns: `Background`

### setDoNotPrint()

Dictates whether the background should be for preview purposes only. It is `true` by default and will not be printed. If you wish for the background to be printed, pass `false` to this method. It takes a *boolean*.

Returns: `Background`

!> If the background is intended for preview purposes only, the background element will still be present in the final SVG file. However, it contains a "do not print" instruction to ensure it is stripped out when being processed for printing by the server-side Plateit API. If you want to remove it entirely from the SVG document, un-utilise it using the `utilise()` method instead (see below).

### utilise()

Toggle the Background component on or off. It takes a *boolean*.

Returns: `Background`

### isUtilised()

Use to check if the Background component is being utilised or not.

Returns: `boolean`

### reset()

Resets the Background properties to the defaults.

Returns: `Background`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised Background properties.

Returns: `object`

### freshProperties()

Resets the Background properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `Background`