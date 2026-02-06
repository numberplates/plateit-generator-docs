# Bsau

The design properties for the bsau component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **text** | string\|array | 'BSAU 145E' | The bsau text. |
| **textFontSrc** | string | '' | The path or url to the font file. |
| **textLineHeight** | number | 2 | The height in mm of the text. |
| **textColour** | string\|array | 'black' | The [colour](/other/colour.md) of the text. |
| **isInBorder** | boolean | false | Embeds the bsau into the border if true |

!> The Bsau component has no effect on shaped plates. Use the `bottomLineExtra` controller instead. [See here](/examples/shaped.md) for examples.

## Methods <!-- {docsify-ignore} -->

### setText()

Sets the bsau text. It takes a *string*, or an *array* of strings for multiple lines.

Returns: `Bsau`

### setTextFont()

Sets the desired font. It takes a *string* consisting of a relative path to the font file, or a fully formed URL.

Returns: `Bsau`

### setTextLineHeight()

Sets the height of the text in mm. It takes a *number*.

Returns: `Bsau`

### setTextColour()

Sets the [colour](/other/colour.md) of the text. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `Bsau`

### setInBorder()

The bsau can be embedded in the border. It takes a *boolean*.

Returns: `Bsau`

### utilise()

Toggle the bsau component on or off. It takes a *boolean*.

Returns: `Bsau`

### isUtilised()

Use to check if the bsau component is being utilised or not.

Returns: `boolean`

### reset()

Removes (un-utilises) the bsau component and resets its design properties to the defaults.

Returns: `Bsau`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised bsau design properties.

Returns: `object`

### freshProperties()

Resets all bsau design properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `Bsau`