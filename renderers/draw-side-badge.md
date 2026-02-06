# DrawSideBadge

## Methods <!-- {docsify-ignore} -->

### render()

Draws the side badge.

Returns: `Promise<boolean>`

### getCoverMetrics()

Calculates and returns dimension and positioning metrics for a centralised cover image *before* any user-specified offset positioning has occurred.

It returns two nested objects:

1. The default position and overflow data of the cover at its default, fitted scale.
2. The position and overflow data of the cover at an explicitly defined scale if different.

**Note:** the returned coordinates are in the coordinate space of the side badge's background rectangle element, not the outer document's.

!>The side badge cover must be rendered before calling.

Returns: `object`

### readjustCoverPlacement()

Readjusts the scale and position of an existing cover image element without having to re-fetch the image file and re-build the entire side badge.

!>The side badge cover must be rendered before calling.

Returns: `DrawSideBadge`