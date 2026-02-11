# Example Shaped Plates

## Shaped Plate

![Shaped plate preview](images/shaped.svg)

```javascript
// Document.
plate.document
  .setWidth(639)
  .setHeight(179)

// Background.
plate.background
  .setBackgroundColour('yellow')
  .setShape('../assets/shapes/JaguarXTypeEst_639x179.svg')
  .utilise(true)

// Reg.
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line.
plate.bottomLine
  .setText('Acme Number Plates SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bottom Line Extra.
plate.bottomLineExtra
  .setText('Acme BSAU 145e')
  .setTextHeight(3)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Render.
plate.render()
```

## Shaped Plate With Border and Side Badge

![Shaped plate preview](images/shaped-with-border-and-side-badge.svg)

> A side badge on a shaped plate will be as tall as its boundary permits in the shape's template file (see image). If you'd prefer it to be the same height as the registration, use a "floating" side badge instead, as per the next example.

```javascript
// Document.
plate.document
  .setWidth(639)
  .setHeight(179)

// Background.
plate.background
  .setBackgroundColour('yellow')
  .setShape('../assets/shapes/JaguarXTypeEst_639x179.svg')
  .utilise(true)

// Reg.
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line.
plate.bottomLine
  .setText('Acme Number Plates SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bottom Line Extra.
plate.bottomLineExtra
  .setText('Acme BSAU 145e')
  .setTextHeight(3)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Border.
plate.border
  .setThickness(2)
  .setColour('black')
  .utilise(true)

// Left Side Badge.
plate.sideBadgeLeft
  .setWidth(44)
  .setBackgroundColour('blue')
  .setImage('../assets/badges/FlagUnionJack.svg')
  .setText(['UNITED', 'KINGDOM'])
  .setTextFont('../assets/fonts/OpenSans-ExtraBold.ttf')
  .setInsideBorder(true)
  .utilise(true)

// Render.
plate.render()
```

## Shaped Plate With Border and Floating Side Badge

![Shaped plate preview](images/shaped-with-border-and-floating-side-badge.svg)

```javascript
// Document.
plate.document
  .setWidth(639)
  .setHeight(179)

// Background.
plate.background
  .setBackgroundColour('yellow')
  .setShape('../assets/shapes/JaguarXTypeEst_639x179.svg')
  .utilise(true)

// Reg.
plate.reg
  .setText('NG25 XYZ')
  .setTextColour('black')
  .setTextHeight(79)
  .setTextFont('../assets/fonts/CharlesWright-Car.ttf')
  .utilise(true)

// Bottom Line.
plate.bottomLine
  .setText('Acme Number Plates SW1A 2AA')
  .setTextHeight(4)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Bottom Line Extra.
plate.bottomLineExtra
  .setText('Acme BSAU 145e')
  .setTextHeight(3)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Border.
plate.border
  .setThickness(2)
  .setColour('black')
  .utilise(true)

// Left Side Badge.
plate.sideBadgeLeft
  .setWidth(44)
  .setBackgroundColour('blue')
  .setImage('../assets/badges/FlagUnionJack.svg')
  .setText(['UNITED', 'KINGDOM'])
  .setTextFont('../assets/fonts/OpenSans-ExtraBold.ttf')
  .setFloating(true)
  .setInsideBorder(true)
  .utilise(true)

// Render.
plate.render()
```
