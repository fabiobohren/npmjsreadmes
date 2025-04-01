# Scanbot Cordova Barcode Scanner SDK

## About the Scanbot Barcode Scanner SDK?

The Scanbot [Barcode Scanner SDK](https://scanbot.io/barcode-scanner-sdk/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites) provides intuitive APIs to integrate fast, reliable barcode scanning into your Cordova app.

It works entirely offline and scans barcodes in 0.04 seconds, even in challenging conditions like poor lighting or with damaged codes.

💡 For more details, check out our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/cordova/introduction/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites) or see our [example app](https://github.com/doo/scanbot-barcode-scanner-sdk-example-cordova-ionic).

### Supported barcode types

Our library supports all common 1D and 2D barcodes and multiple postal symbologies, including:

| Barcode type       | Symbologies                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1D Barcodes        | [EAN](https://scanbot.io/barcode-scanner-sdk/ean/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [UPC](https://scanbot.io/barcode-scanner-sdk/upc/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Code 128](https://scanbot.io/barcode-scanner-sdk/code-128/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [GS1-128](https://scanbot.io/barcode-scanner-sdk/gs1-128/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Code 39](https://scanbot.io/barcode-scanner-sdk/code-39/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Codabar](https://scanbot.io/barcode-scanner-sdk/codabar/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [ITF](https://scanbot.io/barcode-scanner-sdk/itf-code/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), Code 25, Code 32, Code 93, Code 11, MSI Plessey, Standard 2 of 5, IATA 2 of 5, Databar (RSS), GS1 Composite                                                                                                                                                               |
| 2D Barcodes        | [QR Code](https://scanbot.io/glossary/qr-code/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Micro QR Code](https://scanbot.io/barcode-scanner-sdk/micro-qr-code/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Aztec Code](https://scanbot.io/barcode-scanner-sdk/aztec-code/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [PDF417 Code](https://scanbot.io/barcode-scanner-sdk/pdf417/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Data Matrix Code](https://scanbot.io/barcode-scanner-sdk/data-matrix/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [GiroCode](https://scanbot.io/glossary/giro-code/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [PPN](https://scanbot.io/glossary/ppn/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [UDI](https://scanbot.io/glossary/udi/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), [Royal Mail Mailmark](https://scanbot.io/barcode-scanner-sdk/royal-mail/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites), MaxiCode |
| Postal Symbologies | USPS Intelligent Mail Barcode (IMb), Royal Mail RM4SCC Barcode, Australia Post 4-State Customer Code, Japan Post 4-State Customer Code, KIX                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

💡 Please visit our [docs](https://docs.scanbot.io/barcode-scanner-sdk/cordova/supported-barcodes/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites) for a complete overview of the supported barcode symbologies.

### Changelog

For a detailed list of changes in each version, see the [changelog](https://docs.scanbot.io/barcode-scanner-sdk/cordova/changelog/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites).

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

##### Barcode detection

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

## Additional information

### Guides and Tutorials

Integrating the Scanbot Cordova Barcode Scanner plugin into your Cordova app takes just a few minutes, and our step-by-step guides make the process even easier.

💡 Our [Ionic Cordova Barcode Scanner tutorial](https://scanbot.io/techblog/cordova-barcode-scanner-tutorial-how-to-integrate-our-scanning-functionalities/?utm_source=github.com&utm_medium=referral&utm_campaign=dev_sites) walks you through the integration process step by step. Follow along to implement a powerful barcode scanning feature quickly.

Alternatively, check out our [developer blog](https://scanbot.io/techblog/?utm_source=github.com&utm_medium=referral&utm_campaign=dev_sites) for a collection of in-depth tutorials, use cases, and best practices.

### Trial license

The Scanbot SDK will run for one minute per session without a license. After that, all functionalities and UI components will stop working. 

To try the Cordova Barcode Scanner SDK without the one-minute limit, you can request a free, no-strings-attached [7-day trial license](https://scanbot.io/trial/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites).

Our pricing model is simple: Unlimited barcode scanning for a flat annual license fee, full support included. There are no tiers, usage charges, or extra fees. [Contact our team](https://scanbot.io/contact-sales/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites) to receive your quote.

### Free developer support

Need help integrating or testing our Barcode Scanner SDK in your Cordova project? We offer [free developer support](https://docs.scanbot.io/support/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites) via Slack, MS Teams, or email.

As a customer, you also get access to a dedicated support Slack or Microsoft Teams channel to talk directly to your Customer Success Manager and our engineers.
