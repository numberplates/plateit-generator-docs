# Installation

This JavaScript library does not exist in the official NPM registry. However, it can be installed from Plateit's private registry with a valid access token by executing the following command:

```bash
PLATEIT_PACKAGES_TOKEN=your_token_here npm install https://packages.plateit.co.uk/plateit-generator-2.0.1.tgz
```

The above command will *fail* without the following line in your project's `.npmrc` file:

```
//packages.plateit.co.uk/:_authToken=${PLATEIT_PACKAGES_TOKEN}
```

Once installed, it can be imported like so:

```javascript
import { Plate } from 'plateit-generator'
```

NPM will handle the installation of the dependencies for you.

For running the application on a server, please refer to [this short guide](/server.md).

## Direct Link

Alternatively, it can be imported by referencing the "IIFE" version of the script in the header or footer of your html file/s. Its external dependencies must be explicitly referenced first.

```html
<!-- dependencies -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/svg.js/3.2.0/svg.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/opentype.js/1.3.4/opentype.min.js"></script>

<!-- plateit generator -->
<script src="node_modules/plateit-generator/dist/plateit-generator.min.iife.js"></script>
```

You are now ready for the [setup](/setup.md).