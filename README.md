# lockwright-utils-qr

A lightweight utility package for generating QR codes in SVG format. This package provides a simple Promise-based API to create QR codes for URLs, text, or any other data you need to encode.

Site: [lockwright.dexterity.works](https://lockwright.dexterity.works)

Community fork of PearPass (Apache 2.0). Not affiliated with or endorsed by Tether Data or the Pears project.

## Table of Contents

- [Features](#features)
- [Security Notice](#security-notice)
- [Installation](#installation)
- [Usage Examples](#usage-examples)
- [Dependencies](#dependencies)
- [Related Projects](#related-projects)

## Features

- Generate QR codes in SVG format
- Customizable margin settings
- Promise-based API
- Lightweight implementation

## Security Notice

Imports stay `@tetherto/pear-apps-utils-qr`. That npm name is not this fork if you install it from the npm registry.

## Installation

```bash
npm install git+https://github.com/Dexterity-Works/lockwright-utils-qr.git
```

## Usage Examples

```javascript
import { generateQRCodeSVG } from '@tetherto/pear-apps-utils-qr';

// Basic usage
generateQRCodeSVG('https://example.com', { type: 'svg', margin: 4 })
    .then(svgString => {
        // Use the SVG string
        console.log(svgString);
    })
    .catch(error => {
        console.error('Error generating QR code:', error);
    });

// With custom margin
const qrOptions = { type: 'svg', margin: 0 };
const svgOutput = await generateQRCodeSVG('Your text here', qrOptions);
```

## Dependencies

- [qrcode](https://www.npmjs.com/package/qrcode) - QR code generation library

## Related Projects

- [lockwright-app-mobile](https://github.com/Dexterity-Works/lockwright-app-mobile) - Lockwright for mobile
- [lockwright-app-desktop](https://github.com/Dexterity-Works/lockwright-app-desktop) - Lockwright for desktop
- [tether-dev-docs](https://github.com/Dexterity-Works/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.