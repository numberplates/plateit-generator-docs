# Registration

The design properties for the registration component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **text** | string\|array | '' | The registration text. |
| **textFontUrl** | string | '' | The path or url to the font file. |
| **textLineHeight** | number | 79 | The height in mm of the text. |
| **textLineGap** | number | 19 | For multi-line plates, this is the gap in mm between each line. |
| **textColour** | string\|array | 'black' | The [colour](other/colour.md) of the text. |
| **textIsCutOut** | boolean | undefined | [See metal plates](/examples/oblongs.md#metal-oblong).  |

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

Sets the [colour](other/colour.md) of the registration. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `Registration`

### setTextCutOut()

Instructs the text to be cut out of the background. It takes a *boolean*. The text needs to be set to black to work. For an example, please see [metal plates](/examples/oblongs.md#metal-oblong).

Returns: `Registration`

### render()

Renders the registration component only.

Returns: `Promise`

**Note:** The registration is the only component that, when modified, won't interfere with any other component (except for **some** scenarios - [see here](../rendering.md#registration)). For this reason, if you want your application's preview image to refresh upon every key stroke, for increased performance speed, call the targetted `plate.reg.render()` method instead of the generic `plate.render()` method. This will result in quicker render speeds because *only* the reg is being redrawn, instead of the entire plate.

### hasResized()

If the total width or height of the registration exceeds its boundary, the registration will shrink to fit. **This will render the plate illegal for road use**. You can check if the registration has shrunk by calling this method after the render Promise has been fulfilled.

Returns: `boolean`

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