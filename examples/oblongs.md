# Example Oblong Plates

A collection of oblong plates created with the Plateit number plate generator and the code used to create them.

## Standard Oblong

![Oblong plate preview](images/standard-car-oblong.svg)

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Render
plate.render()
```
## Standard Oblong With Side Badge

![Oblong plate preview](images/standard-car-oblong-with-side-badge.svg)

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Left Side Badge
plate.sideBadgeLeft
  .setWidth(44)
  .setBackgroundColour('blue')
  .setImage('../assets/badges/FlagUnionJack.svg')
  .setText(['UNITED', 'KINGDOM'])
  .setTextFont('../assets/fonts/OpenSans-ExtraBold.ttf')
  .utilise(true)

// Render
plate.render()
```

## Standard Oblong With Border and Side Badge

![Oblong plate preview](images/standard-car-oblong-with-border-and-side-badge.svg)

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Border
plate.border
  .setThickness(2)
  .setColour('black')
  .utilise(true)

// Left Side Badge
plate.sideBadgeLeft
  .setWidth(44)
  .setBackgroundColour('blue')
  .setImage('../assets/badges/FlagUnionJack.svg')
  .setText(['UNITED', 'KINGDOM'])
  .setTextFont('../assets/fonts/OpenSans-ExtraBold.ttf')
  .utilise(true)

// Render
plate.render()
```

## Standard Oblong With BSAU in Border

![Oblong plate preview](images/standard-car-oblong-with-bsau-in-border.svg)

> By default, if a border is present, the bsau will sit above it in the bottom-right corner of the plate. It can optionally be embedded into the border itself.

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .setInBorder(true)
  .utilise(true)

// Border
plate.border
  .setThickness(2)
  .setColour('black')
  .utilise(true)

// Render
plate.render()
```

## Standard Oblong 4D

![Oblong plate preview](images/standard-car-oblong-4d.svg)

> The "4D" font file is being used to create the raised effect. **This should be used for customer previews only**. It will be printed like this if it is not removed!

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car-4D.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Render
plate.render().then(() => {

  // 3D/4D Letters are pre-cut to a specific size and stuck on.
  // If the reg has been shrunk to fit, it won't work.
  
  if(plate.renderers.reg.hasRegResized()) {
    alert('The reg is too long to accomodate 3D/4D letters')
  }

})
```

## Standard Oblong 4D Stacked

![Oblong plate preview](images/standard-car-oblong-4d-stacked.svg)

> The raised effect is being created by stacking multiple [registration layers](/additional/registration-overlay-store.md). Unlike the previous "4D" font example, this version doesn't require a separate preview file because the lighter-opacity reg has been set to `doNotPrint`.

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg (this layer will *not* be printed)
plate.reg
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .setTextOffset(-3, 0)
  .setTextColour('black@0.6')
  .setDoNotPrint(true) // <-- Tells Plateit to ignore this layer when printing.
  .utilise(true)

// Reg Overlay (this layer *will* be printed)
plate.regOverlays
  .createLayer()
  .setText('NG25 XYZ')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .setTextColour('black')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Render
plate.render().then(() => {

  // 3D/4D Letters are pre-cut to a specific size and stuck on.
  // If the reg has been shrunk to fit, it won't work.
  
  if(plate.renderers.reg.hasRegResized()) {
    alert('The reg is too long to accomodate 3D/4D letters')
  }

})
```

## Standard Oblong 3D Effect

![Oblong plate preview](images/standard-car-oblong-3d-effect.svg)

> The (printed) 3D effect consists of two fonts stacked on top of each other. It's no longer considered legal for road use.

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour('yellow')
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black@0.7')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Reg Overlay
plate.regOverlays
  .createLayer()
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car-Overlay-3D.ttf')
  .utilise(true)

// Bottom Line
plate.bottomLine
  .setText('ACME Number Plates, SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bsau
plate.bsau
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .setTextHeight(2)
  .utilise(true)

// Render
plate.render()
```
## Metal Oblong

![Oblong plate preview](images/metal-car-oblong.svg)

```javascript
// Document
plate.document
  .setWidth(520)
  .setHeight(111)

// Background
plate.background
  .setBackgroundColour(['lightgray', 'gray', 'y'])
  .utilise(true)

// Reg
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .setTextCutOut(true)
  .utilise(true)

// Border
plate.border
  .setThickness(0)
  .setInnerColour('black')
  .setInnerMargin(5)
  .utilise(true)

// Render
plate.render()
```