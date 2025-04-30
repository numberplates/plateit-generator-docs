# RegistrationOverlayStore

Allows the layering of further [Registration](/components/registration.md) components. This is useful when fonts need to be stacked, or for when you need to create a raised effect to convey laser-cut 3D/4D characters.

Each layer is stored in a class property array, with higher indices representing layers that are positioned further in front, beginning with zero for the first layer. [See here](/examples/oblongs.md#standard-oblong-3d-effect) for an example.

## Methods <!-- {docsify-ignore} -->

### createLayer()

Creates a new registration overlay and returns its [Registration](/components/registration.md) object.

Returns: `Registration`

### getLayer()

Returns the layer at the given index. It takes a *number*.

Returns: `Registration`

### deleteLayer()

Deletes the layer at the given index. It takes a *number*.

Returns: `RegistrationOverlayStore`

> Note: The indices are reset with each deletion. For instance, if you have three layers at indices 0, 1, and 2, and you delete the layer at index 1, the indices of the remaining layers will be updated to 0 and 1.

### deleteAllLayers()

Deletes all layers.

Returns: `RegistrationOverlayStore`

### getLayerCount()

Returns the amount of layers.

Returns: `number`

### isUtilised()

Returns true if *any* of the layers are utilised.

Returns: `boolean`