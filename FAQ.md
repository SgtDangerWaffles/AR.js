# Frequently Asked Questions (FAQ)

Welcome to the AR.js FAQ! This document addresses common questions about using AR.js. If you don't find an answer here, please check the [official documentation](https://ar-js-org.github.io/AR.js-Docs/) or ask on [StackOverflow](https://stackoverflow.com/search?q=ar.js) or our [Gitter chat](https://gitter.im/AR-js/Lobby).

## Table of Contents

- [Getting Started](#getting-started)
- [Image Tracking](#image-tracking)
- [Marker Tracking](#marker-tracking)
- [Location-Based AR](#location-based-ar)
- [Troubleshooting](#troubleshooting)
- [Performance](#performance)
- [Browser Compatibility](#browser-compatibility)

## Getting Started

### What is AR.js?

AR.js is a lightweight library for Augmented Reality on the Web, featuring Image Tracking, Location-based AR, and Marker tracking. It works on both desktop and mobile browsers.

### Which version should I use?

AR.js comes in two builds:
- **AR.js with Image Tracking + Location Based AR** - Use this if you need NFT (Natural Feature Tracking)
- **AR.js with Marker Tracking + Location Based AR** - Use this for marker-based AR

Choose the one that fits your project needs. Don't import both builds in the same project.

### Do I need a server to run AR.js?

Yes, AR.js requires HTTPS (except on localhost) because it needs camera access. You can use:
- Local development servers (http-server, live-server, etc.)
- GitHub Pages
- Any web hosting with HTTPS support

### Can I use AR.js offline?

AR.js can work offline if you host all assets locally and the page is cached. However, initial camera permission requires an active connection.

## Image Tracking

### How do I create image descriptors for NFT?

You need to use the NFT Marker Creator tool. Check the [official documentation](https://ar-js-org.github.io/AR.js-Docs/) for detailed instructions on creating image descriptors.

### What makes a good tracking image?

Good tracking images should:
- Have high contrast
- Contain distinct features (corners, patterns)
- Be at least 480x480 pixels
- Avoid uniform colors or gradients
- Have asymmetric patterns

### Why is my image tracking not working?

Common issues:
- Image descriptors not properly generated
- CORS issues with hosted assets
- Poor lighting conditions
- Image too small or too large in real world
- Low-contrast or uniform images

## Marker Tracking

### What markers can I use?

AR.js supports:
- Built-in markers: `hiro`, `kanji`
- Custom markers generated with the AR.js marker training tools
- Barcode markers

### How do I create custom markers?

Use the [AR.js Marker Generator](https://ar-js-org.github.io/AR.js/three.js/examples/marker-training/examples/generator.html) to create custom pattern markers.

### What's the difference between pattern and barcode markers?

- **Pattern markers**: Custom images that can be unique to your application
- **Barcode markers**: Numerical markers (0-63) that are easier to generate but less unique

## Location-Based AR

### Why isn't location-based AR working?

Check these common issues:
- GPS permissions not granted
- Location services disabled on device
- Poor GPS signal (indoor environments)
- Coordinates not set correctly
- Device compass not calibrated

### What's the accuracy of location-based AR?

Location-based AR accuracy depends on:
- GPS signal quality (typically 5-10m accuracy)
- Device sensors quality
- Environmental factors (buildings, weather)
- Compass calibration

### Can I use location-based AR indoors?

Indoor GPS accuracy is very poor. Location-based AR works best outdoors with clear sky visibility.

## Troubleshooting

### Camera not starting

1. Check HTTPS is enabled (required for camera access)
2. Grant camera permissions in browser
3. Check if another app is using the camera
4. Try a different browser
5. Clear browser cache and reload

### Content not appearing

1. Verify marker/image is properly positioned in camera view
2. Check console for errors (CORS, loading issues)
3. Ensure lighting is adequate
4. Verify assets are loading correctly
5. Check if content is positioned correctly (scale, position parameters)

### CORS errors

Use a CORS proxy or host assets on the same domain. Example:
```
https://arjs-cors-proxy.herokuapp.com/[your-asset-url]
```

Or configure your server to allow CORS.

### AR content is jittery or unstable

Try adjusting smoothing parameters:
```html
<a-nft
  smooth="true"
  smoothCount="10"
  smoothTolerance=".01"
  smoothThreshold="5"
>
```

## Performance

### How can I improve performance?

1. Reduce 3D model complexity (polygon count)
2. Optimize texture sizes
3. Use appropriate tracking method for your use case
4. Test on target devices (mobile performance varies)
5. Minimize other JavaScript processing
6. Use `renderer="logarithmicDepthBuffer: true;"` cautiously

### What devices are supported?

AR.js works on:
- Modern smartphones (iOS Safari, Android Chrome)
- Desktop browsers with webcam
- Tablets

Performance is best on:
- iOS: iPhone 8 and newer
- Android: Mid to high-end devices with good GPU

## Browser Compatibility

### Which browsers support AR.js?

AR.js works on browsers that support:
- WebGL
- getUserMedia (camera access)
- WebRTC

**Supported browsers:**
- Chrome/Chromium (Android, Desktop)
- Safari (iOS, macOS)
- Firefox (with some limitations)
- Edge (Chromium-based)

**Not supported:**
- Internet Explorer
- Older browser versions without WebGL

### Why doesn't it work in my browser?

1. Update to the latest browser version
2. Check WebGL support: https://get.webgl.org/
3. Ensure camera permissions are granted
4. Try a different browser

## Still Have Questions?

- **Documentation**: [AR.js Official Documentation](https://ar-js-org.github.io/AR.js-Docs/)
- **StackOverflow**: [AR.js questions](https://stackoverflow.com/search?q=ar.js)
- **Gitter Chat**: [AR.js community](https://gitter.im/AR-js/Lobby)
- **GitHub Issues**: For bugs and feature requests only (see [CONTRIBUTING.md](CONTRIBUTING.md))
- **Old Repository**: [Legacy AR.js issues](https://github.com/jeromeetienne/AR.js/issues) (search closed issues)
