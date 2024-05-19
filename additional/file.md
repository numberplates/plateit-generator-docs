# File

This object is responsible for handling import and export functionality. More information can be found on the [import/export](other/import-export.md) page.

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

Promises to return the final design as an SVG string. By default it will include all design metadata, this can be turned off by passing `false`. However, doing so will prevent it from being re-imported later. It takes a *boolean*.

Returns: `Promise<string>`

### extractMetadataFromSvg()

Takes an SVG string exported from this application and returns its design metadata as an object. It takes a *string*.

Returns: `object`