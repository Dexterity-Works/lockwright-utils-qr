> [!WARNING]
> 🍐 PearPass is currently paused from active development, so please use at your own caution until further notice.

# pear-apps-utils-qr

A lightweight utility package for generating QR codes in SVG format. This package provides a simple Promise-based API to create QR codes for URLs, text, or any other data you need to encode.

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

1. To ensure the security and integrity of your projects, please note that official PearPass packages are distributed exclusively through our GitHub organization.
2. Any packages with similar names found on the npm registry or other third-party package managers are not affiliated with PearPass and should be strictly avoided. We recommend installing directly from this repository to ensure you are using the verified, open-source version.

## Installation

```bash
npm install git+https://github.com/tetherto/pear-apps-utils-qr.git
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

- [@tetherto/pearpass-app-mobile](https://github.com/tetherto/pearpass-app-mobile) - A mobile app for PearPass, a password manager
- [@tetherto/pearpass-app-desktop](https://github.com/tetherto/pearpass-app-desktop) - A desktop app for PearPass, a password
- [@tetherto/tether-dev-docs](https://github.com/tetherto/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.