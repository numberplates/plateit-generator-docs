# Rendering

To render the plate, call the `render()` method inside the main Plate object. It returns a Promise. If you want to execute some code only after a successful render, you'll need to wait until the Promise has been fulfilled.

For example (note the `await` keyword):

```javascript
await plate.render()

const wasRegShrunk = plate.hasRegResized()

if(wasRegShrunk) {
  alert('The reg was shrunk to fit and therefore is no longer legal!')
}
```