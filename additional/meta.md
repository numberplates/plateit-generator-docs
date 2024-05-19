# Meta

When an SVG is [exported](other/import-export.md) from this application, it will include XML metadata of **all design properties**. Additional, non-design metadata can be added using the methods outlined on this page and will be found further nested under the `<meta>` key.

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **meta** | object | {} | Extra data you wish to include. |

> Note: upon [export](other/import-export.md), the app version will be added to the meta object.

## Methods <!-- {docsify-ignore} -->

### setProperty()

Sets a metadata property. It takes a *string* for the key and *mixed* data types for the value.

Returns: `Meta`

### getProperty()

Retrieves a previously set metadata property. It takes a *string* (the key).

Returns: `mixed`

### deleteProperty()

Deletes a previously set metadata property. It takes a *string* (the key).

Returns: `Meta`

### getProperties()

Returns all metadata.

Returns: `object`

### freshProperties()

Removes all metadata properties and overwrites them with any new ones. It takes an *object*.

Returns: `Meta`

### isUtilised()

Returns true if there is any metadata present.

Returns: `boolean`