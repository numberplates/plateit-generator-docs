# SideBadge

The design properties for the side badge component are as follows:

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **width** | number | 45 | The side badge width. |
| **innerMargin** | number | 3 | The gap between the inside of the badge and the content. |
| **radius** | number | 3 | The radius of the badge's corners. |
| **isInsideBorder** | boolean | false | Positions the badge inside the border. |
| **isFloating** | boolean | false | For legal, multi-line plates (see below). |
| **imageUrl** | string | null | The path or url to the image file. |
| **text** | string\|array | '' | The side badge text. |
| **textFontUrl** | string | '' | The path or url to the font file. |
| **textColour** | string\|array | 'white' | The [colour](/other/colour.md) of the text. |
| **textIsCutOut** | boolean | null | Cuts out the text from the background.  |

## Methods <!-- {docsify-ignore} -->

### setWidth()

Sets the width of the side badge in mm. It takes a *number*.

Returns: `SideBadge`

### setBackgroundColour()

Sets the [colour](/other/colour.md) of the background. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `SideBadge`

### setInnerMargin()

Sets the inner margin of the side badge in mm. It takes a *number*.

Returns: `SideBadge`

### setRadius()

Sets the radius of the side badge's corners in mm. It takes a *number*.

Returns: `SideBadge`

### setInsideBorder()

The side badge can be positioned either inside or outside of the border. By default it is set to outside. It takes a *boolean*.

Returns: `SideBadge`

### setFloating()

The only way (most) multi-line plates can have a side badge and still be legal is if the side badge is "floating". A floating side badge is rendered at the same height as the registration text and is automatically positioned next to the shortest line of the multi-line registration. [Click here for an example](/examples/squares#standard-car-square-with-border-and-floating-side-badge). It will not work if the side badge is positioned outside of the border. It takes a *boolean*.

Returns: `SideBadge`

### isFloating()

Returns true or false depending on whether the side badge is set to "floating".

Returns: `Boolean`

### setImage()

Sets the desired flag image. It takes a *string* consisting of a relative path to the image file, or a fully formed URL.

**Note:** it accepts SVG files only.

Returns: `SideBadge`

### setText()

Sets the side badge text. It takes a *string*, or an *array* of strings for multiple lines.

Returns: `SideBadge`

### setTextFont()

Sets the desired font. It takes a *string* consisting of a relative path to the font file, or a fully formed URL.

Returns: `SideBadge`

### setTextColour()

Sets the [colour](/other/colour.md) of the text. It takes a *string* for a solid colour, or an *array* of strings for a gradient.

Returns: `SideBadge`

### setTextCutOut()

Instructs the text to be cut out of the background. It takes a *boolean*. The text needs to be set to black to work.

Returns: `SideBadge`

### utilise()

Toggle the side badge component on or off. It takes a *boolean*.

Returns: `SideBadge`

### isUtilised()

Use to check if the side badge component is being utilised or not.

Returns: `boolean`

### reset()

Removes (un-utilises) the side badge component and resets its design properties to the defaults.

Returns: `SideBadge`

### getProperty()

Returns the value of a design property. It takes a *string* (the key of the property to return).

Returns: `mixed`

### getProperties()

Returns all of the utilised side badge design properties.

Returns: `object`

### freshProperties()

Resets all side badge design properties to the defaults and overwrites them with any new ones. It takes an *object*.

Returns: `SideBadge`