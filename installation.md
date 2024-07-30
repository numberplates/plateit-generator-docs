# Installation

## ESM Modules

This javascript library does not exist in the NPM registry. It must be installed manually by running the following command, being sure to reference the correct location of the package file on your local machine:

```bash
npm install /local/path/to/plateit-generator.tgz
```

Once installed, it can be imported like so:

```javascript
import { Plate } from 'plateit-generator'
```

NPM will handle the installation of the dependencies for you.

For running the application on a server, please refer to [this short guide](server.md).

## Direct Link

Alternatively, it can be imported by referencing the "IIFE" version of the script in the header or footer of your html file/s. Its dependencies must be explicitly referenced first.

```html
<!-- dependencies -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/svg.js/3.2.0/svg.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/opentype.js/1.3.4/opentype.min.js"></script>

<!-- plateit generator -->
<script src="path/to/plateit-generator.min.iife.js"></script>
```

You are now ready for the [setup](setup.md).