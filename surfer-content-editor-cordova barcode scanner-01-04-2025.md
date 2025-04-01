## How to use the SDK

### Installation

#### Requirements

Check out our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/cordova/introduction/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#requirements) for a full overview of our SDK's requirements. For a detailed explanation on setting up our Cordova barcode scanner Plugin, see our [full installation guide](https://docs.scanbot.io/barcode-scanner-sdk/cordova/getting-started/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites).

#### Install steps

Install the Scanbot Barcode Scanner SDK module by running the following command in your root project folder:

```
$ cordova plugin add cordova-plugin-scanbot-barcode-scanner
```

Or in an [Ionic](https://ionicframework.com/)-based project:

```
$ ionic cordova plugin add cordova-plugin-scanbot-barcode-scanner
```

### AndroidX Configuration

By default, Cordova does not enable [AndroidX](https://developer.android.com/jetpack/androidx) in a new project. The AndroidX libraries – also called [Android Jetpack libraries](https://developer.android.com/jetpack) – replace the old *Android Support Library*. They are required by most modern plugins, including the Scanbot Barcode SDK plugin. To enable AndroidX, we have to add the following preference entry in the config.xml file of our project:

```
<platform name="android">
  <preference name="AndroidXEnabled" value="true" />
</platform>
```

### Basic Implementation

#### Initialize the SDK

The Scanbot SDK for Cordova must be initialized before usage:

```
TBD
```

💡 You can test the SDK without a license key for 60 seconds per app session. Need longer testing? Get your [free trial license key](https://scanbot.io/trial/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites).

#### Implement the Barcode Scanner SDK

```
TBD
```

### Barcode scanner configuration

The Scanbot Cordova Barcode Scanner Plugin offers two options for implementing the barcode scanning UI: the standard single barcode scanner and the batch scanner mode.

💡 For a full overview of the SDK's supported configuration options, visit our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/cordova/barcode-scanner/barcode-scanner-ui/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites).

#### Barcode Scanner UI

This is the default configuration. It is optimized for detecting a single barcode at a time. The Barcode Scanner UI offers numerous optional customization options, including:

##### Visual elements:

The SDK's visual customization options allow you to configure the appearance of different UI elements to your needs, such as the view finder, the barcode detection overlay, the top bar, button labels, or user guidance elements.

```
// Example for configuring the SDK´s visual elements
var visualConfig = {
  finderLineColor: '#ff0000',               // Red finder line
  topBarBackgroundColor: '#212121',         // Dark gray top bar
  cancelButtonTitle: 'Exit Scanner'         // Custom cancel button text
};
```

##### Camera controls

You can also adjust certain camera control functions, such as zoom levels, focus settings, orientation lock, or the camera preview mode.

```
// Example for configuring the SDK´s camera controls
var cameraConfig = {
  cameraZoomFactor: 0.5,                    // Initial zoom at 50%
  focusLockEnabled: true,                   // Lock focus
  orientationLockMode: 'PORTRAIT'           // Lock to portrait orientation
};
```

##### Barcode detection settings

Additionally, the SDK comes with additional filters for detecting  barcode formats or settings to handle specific barcode types, such as for GS1 parising.

```
// Example for configuring the SDK´s barcode detection settings
var detectionConfig = {
  // Only detect specific barcodes
  barcodeFormats: ['QR_CODE', 'EAN_13', 'CODE_128'],
  
  // Implement specialized Handling for specifc barcodes.
  gs1HandlingMode: 'PARSE'
};
```

##### User experience

Lastly, the SDK provides you with additional settings to improve the user experience, including audio confirmations, auto-cancel timeouts, and touch controls, including pinch-to-zoom and double-tap shortcuts.

```
// Example for configuring additional user experience features
var uxConfig = {
  // Sounds
  successBeepEnabled: true,               // Play sound on successful scan

  // Touch Gestures
  pinchToZoomEnabled: true,               // Enable pinch to zoom
  doubleTapToZoomEnabled: true,           // Enable double-tap to zoom
};
```

#### Batch Barcode Scanner UI

The barcode scanner can also be configured to scan multiple barcodes in succession (without closing the scanning screen every time), to capture more than one barcode from the camera view at once, or to count the scanned items.

#### Data Parsers

The Scanbot Barcode Scanner SDK supports a variety of data parsers that extract structured barcode data from 2D symbologies such as QR Codes and Data Matrix. These include parsers for documents such as driving licences (AAMVA), boarding passes, medical certificates, SEPA forms, Swiss QR codes, and vCard business cards.

💡 Please refer to our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/cordova/supported-barcodes/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#data-parsers) for a full list of supported data parsers.

