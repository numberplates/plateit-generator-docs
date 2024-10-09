# Server Setup

Running the application on a Node server requires an extra step.

At the top of your server-side JavaScript file, along with the Plate class, you need to import two SVG.JS dependencies which have already been installed for you automatically.

```javascript
import { Plate } from 'plateit-generator'
import { registerWindow } from '@svgdotjs/svg.js'
import { createSVGWindow } from 'svgdom'
```

Before invoking the Plate class, include the following code block.

```javascript
const window = createSVGWindow()
registerWindow(window, window.document)
```

This tells the application to use a pseudo window object in place of the client-side window object.