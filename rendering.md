# Rendering

The main Plate object has a `render()` method, and so does each of its [components](objects.md).

It's important to understand the difference to help optimise for speed.

Calling `plate.render()` will re-draw the entire plate.

Calling `plate.componentName.render()` will re-draw only that specific component if a change has been detected.

**However, usually it's best to just call the main `plate.render()` method.**

This is because spacial changes to one component will often have a knock-on effect to others which will not be rendered if you only call the nested component's `render()` method.

**The only exception is the registration (with caveats)**

## Registration

The registration has no knock-on effects to other components providing that there is no [reg overlay](examples/oblongs.md#standard-oblong-3d-effect) present and there is not a "[floating](components/side-badge.md#setfloating)" side badge.

In these instances, if you wish for the design to re-render on every keystroke of the registration, opt for calling the `plate.reg.render()` method instead to get a slight speed advantage. For example:

```javascript
function onRegKeyPress(plate, reg) {
    
    plate.reg.setText(reg)
    
    if(
        plate.sideBadgeLeft.isUtilised() && plate.sideBadgeLeft.isFloating() ||
        plate.sideBadgeRight.isUtilised() && plate.sideBadgeRight.isFloating() ||
        plate.regOverlay.isUtilised()
    ) {
        // There may be knock-on effects to other components, redraw entire plate
        return plate.render()
    }
    else {
        // There will be no knock-on effects, redraw only the reg
        return plate.reg.render()
    }

}
```
## Promises

It's also important to note that the `render()` methods return a Promise. If, for example, you want to execute some code only after a successful render, you'll need to wait until the Promise has been fulfilled.

For example (note the `await` keyword):

```javascript
await plate.render()

let wasRegShrunk = plate.reg.hasResized()

if(wasRegShrunk) {
    alert('The reg was shrunk to fit and therefore is no longer legal')
}
```