# Side Badge Covers

This number plate generator exclusively works with vectors, with one exception: side badge covers. These let you use a raster image as the artwork for a side badge.

## Setting a Cover

Use `setCover(src)` with an image URL, file path, or data URL like so:

```javascript
plate.sideBadgeLeft
  .setCover('/images/badge.png')
  .utilise(true)
```

Use `setCoverScale(scale)` to adjust the size and `setCoverOffset(x, y)` to adjust the position.

## Saving and Restoring Covers

The rendered SVG embeds the cover image as a data URL. A data URL contains the image itself and can be very large, so repeating it in the design metadata would store the image twice!

When [exporting](/other/import-export.md) an SVG with metadata, `exportSvg(true)` replaces cover data URLs in the metadata with internal references.

For example, this:

```javascript
{
  "coverSrc": "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAUDBAQEAwUEBAQFBQUGBwwIBwcHBw8LCwkMEQ8SEhEPERETFhwXExQaFRERGCEYGh0dHx8fExciJCIeJBweHx7/2wBDAQUFBQcGBw4ICA4eFBEUHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh7/wAARCAXcCMkDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmq..."
}
```

Will become this:

```javascript
{
  "coverSrc": "#SideBadgeLeftCover"
}
```

In other words, the image data stays in the SVG image element only.

On [import](/other/import-export.md), the data URL will be reconstructed from the referenced image inside the SVG file.

## Exporting a Design Object

Cover data urls are included by default when [exporting](/other/import-export.md) objects using `exportObject()`. This keeps the object self-contained for later use with `importObject()`.

Pass `false` to `exportObject(false)` to replace cover data URLs with SVG image references as illustrated above. This object will require the accompanying SVG and cannot be resolved by `importObject()` alone. Regular cover URLs and file paths remain unchanged.

## Plateit Server-Side API

If sending an SVG and an accompanying `design_object` to the [Plateit server-side API](https://numberplates.github.io/plateit-api-docs), you can safely set both export arguments to `false`.

For example:

```javascript
await plate.render()
const svg = await plate.file.exportSvg(false) // No embedded design metadata.
const design_object = plate.file.exportObject(false) // Reference cover images in the SVG.
```

Send both together. This keeps the design object separate from the artwork and stores cover image data only once, in the SVG.