# Objects / Components

## The Plate Object

Let's say you have followed the [installation](/installation.md) and [setup](/setup.md) instructions.

You now have a Plate object under a variable named `plate`.

Each Plate has several different design "components". Each component is represented by its own nested object. Each of these objects has its own public methods which can be used to manipulate them.

## Component Objects

!>These are your controllers.

You can access the plate's design components by referencing the following keys:

| Key | Returns | Info |
| --- | --- | --- |
| `plate.document` | [Document](/components/document.md) | Responsible for setting the document (plate) size. |
| `plate.background` | [Background](/components/background.md) | Responsible for setting the preview background colour. |
| `plate.border` | [Border](/components/border.md) | Responsible for manipulating the border. |
| `plate.reg` | [Registration](/components/registration.md) | Responsible for manipulating the registration. |
| `plate.sideBadgeLeft` | [SideBadge](/components/side-badge.md) | Responsible for manipulating the left side badge. |
| `plate.sideBadgeRight` | [SideBadge](/components/side-badge.md) | Responsible for manipulating the right side badge. |
| `plate.bottomLine` | [BottomLine](/components/bottom-line.md) | Responsible for manipulating the bottom line. |
| `plate.bottomLineExtra` | [BottomLine](/components/bottom-line.md) | Responsible for manipulating an additional bottom line. |
| `plate.bsau` | [Bsau](/components/bsau.md) | Responsible for manipulating the british standard mark. |

## Additional Objects

| Key | Returns | Info |
| --- | --- | --- |
| `plate.regOverlays` | [RegistrationOverlayStore](/additional/registration-overlay-store.md) | Responsible for manipulating the registration overlay layers. |
| `plate.metadata` | [Meta](/additional/meta.md) | Optionally add custom metadata. |
| `plate.file` | [File](/additional/file.md) | Methods related to importing and exporting are contained here. |

## Important Note

!>The properties of each component object are **not** designed to be altered directly.

For example, don't do this:

```javascript
plate.reg._utilisedProperties.text = 'MY REG'
```

Use the object's intended public method, like this:

```javascript
plate.reg.setText('MY REG')
```

The public methods for each component are listed in their respective documentation pages.

## Rendering

To render the plate, call the `render()` method inside the main Plate object. It returns a Promise. If you want to execute some code only after a successful render, you'll need to wait until the Promise has been fulfilled.

For example (note the `await` keyword):

```javascript
await plate.render()

const wasRegShrunk = plate.hasRegResized()

if(wasRegShrunk) {
  alert('The reg was shrunk to fit and therefore is no longer legal!')
}
```