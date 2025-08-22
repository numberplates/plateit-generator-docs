# Example Shaped Plates

## Shaped Plate

![Shaped plate preview](images/shaped.svg)

```javascript
// Document
plate.document
  .setWidth(639)
  .setHeight(179)

// Background
plate.background
  .setBackgroundColour('yellow')
  .setShape('../assets/shapes/JaguarXTypeEst.svg')
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

// Bottom Line Extra
plate.bottomLineExtra
  .setText('BSAU 145e')
  .setTextHeight(2)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
  .utilise(true)

// Render
plate.render()
```

## Shaped Plate With Border and Floating Side Badge

![Shaped plate preview](images/shaped-with-border-and-floating-side-badge.svg)

```javascript
// Document
plate.document
  .setWidth(639)
  .setHeight(179)

// Background
plate.background
  .setBackgroundColour('yellow')
  .setShape('../assets/shapes/JaguarXTypeEst.svg')
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

// Bottom Line Extra
plate.bottomLineExtra
  .setText('BSAU 145e')
  .setTextHeight(2)
  .setTextFont('../assets/fonts/OpenSans-Regular.ttf')
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
  .setFloating(true)
  .setInsideBorder(true)
  .utilise(true)

// Render
plate.render()
```
