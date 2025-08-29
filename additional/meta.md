# Meta

When the final design object is [exported](/other/import-export.md) from this application, it can optionally include additional metadata. This can be useful for preserving intent so a front-end editor can, for example, rehydrate form element selections.

| Key | Expects | Default | Info |
| --- | --- | --- | --- |
| **meta** | object | {} | Extra data you wish to include. |

> Note: upon [export](/other/import-export.md), the app version will be added to the meta object.

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