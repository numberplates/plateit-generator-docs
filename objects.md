# Objects / Components

## The Plate Object

Let's say you have followed the [installation](/installation.md) and [setup](/setup.md) instructions.

You now have a Plate object under a variable named `plate`.

Each Plate has several different design "components". Each component is representated by its own nested object. Each of these objects has its own public methods which can be used to manipulate them.

## Component Objects

You can access the plate's design components by referencing the following keys:

| Key | Returns | Info |
| --- | --- | --- |
| `plate.document` | [Document](/components/document.md) | Responsble for setting the document (plate) size. |
| `plate.background` | [Background](/components/background.md) | Responsble for setting the preview background colour. |
| `plate.border` | [Border](/components/border.md) | Responsble for manipulating the border. |
| `plate.reg` | [Registration](/components/registration.md) | Responsble for manipulating the registration. |
| `plate.sideBadgeLeft` | [SideBadge](/components/side-badge.md) | Responsble for manipulating the left side badge. |
| `plate.sideBadgeRight` | [SideBadge](/components/side-badge.md) | Responsble for manipulating the right side badge. |
| `plate.bottomLine` | [BottomLine](/components/bottom-line.md) | Responsble for manipulating the bottom line. |
| `plate.bsau` | [Bsau](/components/bsau.md) | Responsble for manipulating the british standard mark. |

## Additional Objects

| Key | Returns | Info |
| --- | --- | --- |
| `plate.regOverlays` | [RegistrationOverlayStore](/additional/registration-overlay-store.md) | Responsble for manipulating the registration overlay layers. |
| `plate.metadata` | [Meta](/additional/meta.md) | Optionally add custom metadata. |
| `plate.file` | [File](/additional/file.md) | Methods related to importing and exporting are contained here. |

## Important Note

!>The properties of each object are **not** designed to be altered directly.

For example, don't do this:

```javascript
plate.componentName.exampleProperty = 'foo'
```

Use the object's intended public method, like this:

```javascript
plate.componentName.setExampleProperty('foo')
```

The public methods for each component are listed in their respective documentation pages.