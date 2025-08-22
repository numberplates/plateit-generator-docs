# BottomLine

The design properties for the bottom line component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **text** | string\|array | '' | The bottom line text. |
| **textFontUrl** | string | '' | The path or url to the font file. |
| **textLineHeight** | number | 4 | The height in mm of the text. |
| **textColour** | string\|array | 'black' | The [colour](/other/colour.md) of the text. |
| **alignToCentreReg** | boolean\|null | null | Optionally overrides default positioning for some edge cases ([see here](#setAlignToCentreReg))  |

## Methods <!-- {docsify-ignore} -->

### setText()

Sets the bottom line text. It takes a *string*, or an *array* of strings for multiple lines.

Returns: `BottomLine`

### setTextFont()

Sets the desired font. It takes a *string* consisting of a relative path to the font file, or a fully formed URL.

Returns: `BottomLine`

### setTextLineHeight()

Sets the height of the text in mm. It takes a *number*.

Returns: `BottomLine`

### setTextColour()

Sets the [colour](/other/colour.md) of the text. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `BottomLine`

### setAlignToCentreReg()

Force-aligns the central placement of the bottom line with the central placement of the registration for when the registration has been positioned off-centre to account for the presence of a (non-floating) side badge. This is not the default behaviour but may be desired for certain situations. It takes a *boolean*.

Returns: `BottomLine`

> Note: If you are utilising an extra bottom line, this will affect both.

### utilise()

Toggle the bottom line component on or off. It takes a *boolean*.

Returns: `BottomLine`

### isUtilised()

Use to check if the bottom line component is being utilised or not.

Returns: `boolean`

### reset()

Removes (un-utilises) the bottom line component and resets its design properties to the defaults.

Returns: `BottomLine`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised bottom line design properties.

Returns: `object`

### freshProperties()

Resets all bottom line design properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `BottomLine`