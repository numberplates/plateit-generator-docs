# Registration

The design properties for the registration component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **text** | string\|array | '' | The registration text. |
| **textFontUrl** | string | '' | The path or url to the font file. |
| **textLineHeight** | number | 79 | The height in mm of the text. |
| **textLineGap** | number | 19 | For multi-line plates, this is the gap in mm between each line. |
| **textColour** | string\|array | 'black' | The [colour](/other/colour.md) of the text. |
| **textIsCutOut** | boolean | null | [See metal plates](/examples/oblongs.md#metal-oblong).  |
| **textOffset** | array | null | X and Y text offset in mm. |
| **doNotPrint** | boolean | null | If true, it will be for preview purposes only and will not be printed. |

## Methods <!-- {docsify-ignore} -->

### setText()

Sets the registration text. It takes a *string*, or an *array* of strings for multi-line registrations.

Returns: `Registration`

### setTextFont()

Sets the desired font. It takes a *string* consisting of a relative path to the font file, or a fully formed URL.

Returns: `Registration`

### setTextLineHeight()

Sets the height of the text in mm. It takes a *number*.

Returns: `Registration`

### setTextLineGap()

If the registration text spans across multiple lines, this method will dictate the size of the gap in mm between each line. It takes a *number*.

Returns: `Registration`

### setTextColour()

Sets the [colour](/other/colour.md) of the registration. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `Registration`

### setTextCutOut()

Instructs the text to be cut out of the background. It takes a *boolean*. The text needs to be set to black to work. For an example, please see [metal plates](/examples/oblongs.md#metal-oblong).

Returns: `Registration`

### setTextOffset()

Instructs the offset of text from its default position. It takes an *array* of numbers. The first item is the X offset in mm and the second is the Y offset in mm. For example `[3,5]`. It may be useful when using [registration overlays](/additional/registration-overlay-store.md) to create the impression of 3D text. [See this example](/examples/oblongs.md#standard-oblong-4d-stacked).

Returns: `Registration`

### setDoNotPrint()

Dictates whether the registration should be for preview purposes only. It takes a *boolean*. It may be useful when using [registration overlays](/additional/registration-overlay-store.md) to create the impression of 3D text. [See this example](/examples/oblongs.md#standard-oblong-4d-stacked).

Returns: `Registration`

### utilise()

Toggle the Registration component on or off. It takes a *boolean*.

Returns: `Registration`

### isUtilised()

Use to check if the Registration component is being utilised or not.

Returns: `boolean`

### reset()

Removes (un-utilises) the Registration component and resets its design properties to the defaults.

Returns: `Registration`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised Registration design properties.

Returns: `object`

### freshProperties()

Resets all Registrtation design properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `Registration`