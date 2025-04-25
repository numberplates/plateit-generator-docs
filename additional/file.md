# File

This object is responsible for handling import and export functionality. More information can be found on the [import/export](/other/import-export.md) page.

## Methods <!-- {docsify-ignore} -->

### importObject()

Clears all data and sets a fresh plate representation. It takes a *object*.

Returns: `File`

### exportObject()

Returns the entire plate object, including any custom metadata.

Returns: `object`

### importSvg()

Takes an SVG string, extracts the design metadata and sets a fresh representation of the plate. It takes a *string*.

Returns: `File`

> Note: only SVGs exported by this application will be recognised. It requires the design metadata to understand what's what.

### exportSvg()

Promises to return the final design as an SVG string. By default it will *not* include design metadata, this can be turned on by passing `true`. (Metadata is required if you want to re-import it later.) It takes a *boolean*.

Returns: `Promise<string>`

### importXml()

Takes an XML string enveloped in a `<plate>` element and sets a fresh representation of the plate. It takes a *string*.

Returns: `File`

### exportXml()

Returns the final design as an XML string enveloped in a `<plate>` element.

Returns: `string`

### extractMetadataFromSvg()

Takes an SVG string exported from this application (with metadata) and returns its design metadata as an object. It takes a *string*.

Returns: `object`