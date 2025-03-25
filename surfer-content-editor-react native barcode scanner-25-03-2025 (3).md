# Scanbot React Native Barcode Scanner SDK

## Table of contents

### [About the Scanbot Barcode Scanner SDK](#about-the-scanbot-barcode-scanner-sdk)
* [Supported barcode types](#supported-barcode-types)
* [Changelog](#changelog)

### [How to use the SDK](#how-to-use-the-sdk)
* [Installation](#installation)
  * [Requirements](#requirements)
  * [Install steps](#install-steps)
  * [Camera permissions](#camera-permissions)
  * [SDK initialization](#sdk-initialization)
* [Barcode scanner setup](#barcode-scanner-setup)
  * [Scanning modes](#scanning-modes)
  * [Configuration options](#configuration-options)
  * [UI customization](#ui-customization)

### [Additional information](#additional-information)
* [Trial license](#trial-license)
* [Free developer support](#free-developer-support)

## About the Scanbot Barcode Scanner SDK?

The Scanbot Barcode Scanner SDK provides intuitive APIs to integrate fast, reliable barcode scanning into your React Native app.

It works entirely offline and scans barcodes in 0.04 seconds, even in challenging conditions like poor lighting or with damaged codes.

> 💡 For more details, check out our documentation or see our example app.

### Supported barcode types

Our library supports all common 1D and 2D barcodes and multiple postal symbologies, including:

| Barcode type       | Symbologies                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1D Barcodes        | EAN, UPC, Code 128, GS1-128, Code 39, Codabar, ITF, Code 25, Code 32, Code 93, Code 11, MSI Plessey, Standard 2 of 5, IATA 2 of 5, Databar (RSS), GS1 Composite |
| 2D Barcodes        | QR Code, Micro QR Code, Aztec Code, PDF417 Code, Data Matrix Code, GiroCode, NTIN Code, PPN, UDI, Royal Mail Mailmark, MaxiCode                                 |
| Postal Symbologies | USPS Intelligent Mail Barcode (IMb), Royal Mail RM4SCC Barcode, Australia Post 4-State Customer Code, Japan Post 4-State Customer Code, KIX                     |

💡 Please visit our docs for a complete overview of the supported barcode symbologies.

### Changelog

For a detailed list of changes in each version, see the changelog.

## How to use the SDK

### Installation

#### Requirements

Check out our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/react-native/introduction/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#requirements) for a full overview of our SDK's requirements.

#### Install steps

Install the Scanbot Barcode Scanner SDK module by running:

```
// Using Yearn
yarn add react-native-scanbot-barcode-scanner-sdk

// Using npm
npm install react-native-scanbot-barcode-scanner-sdk

// Using Expo
npx expo install react-native-scanbot-barcode-scanner-sdk
```

##### Expo Integration

Expo projects require a development build. Configure the project using our config plugin by adding this to your app config file:

```
"plugins": [
  [
    "react-native-scanbot-barcode-scanner-sdk",
    {
      "iOSCameraUsageDescription": "Barcode Camera permissions",
      "androidCameraPermission": true,
      "androidCameraFeature": true,
      "mavenURLs": true
    }
  ]
],
```

> 💡 See our [full installation guide](https://docs.scanbot.io/barcode-scanner-sdk/react-native/detailed-setup-guide/installation/) for complete details.

#### Camera permissions

Our SDK needs camera access to scan from a live camera stream.

> 💡If you use Expo, the permissions can be configured using our config plugin, and this step can be skipped.

##### Android[​](https://docs.scanbot.io/barcode-scanner-sdk/react-native/detailed-setup-guide/permissions/#android)

Add these camera permissions to your **android/app/src/main/AndroidManifest.xml**:

```
<uses-permission android:name="android.permission.CAMERA" />
<uses-feature android:name="android.hardware.camera" />
```

We added the uses-feature tag for better recognition in the Google Play Store ([learn more](https://developer.android.com/guide/topics/manifest/uses-feature-element)). Our Ready-to-Use UI Components handle runtime permissions automatically.

##### iOS[​](https://docs.scanbot.io/barcode-scanner-sdk/react-native/detailed-setup-guide/permissions/#ios)

Add this camera permission description to **ios/{projectName}/Info.plist** inside the <dict> element:

```
<key>NSCameraUsageDescription</key>
<string>Camera permission is needed to scan barcodes</string>
```

#### SDK initialization

Initialize the SDK before using any features, ideally when your app launches.

Add this import to the top of your file:

```
import ScanbotBarcodeSDK from 'react-native-scanbot-barcode-scanner-sdk'
```

Initialize the SDK with:

```
ScanbotBarcodeSDK
.initializeSdk({ licenseKey: "" })
.then(result => console.log(result))
.catch(err => console.log(err));
```

> 💡 You can test the SDK without a license key for 60 seconds per app session. Need longer testing? Get your free trial license key.

### Barcode scanner setup

#### Scanning modes

The Scanbot Barcode Scanner SDK offers the following scan modes right out-of-the-box, in our ready-to-use UI.

##### Single Scanning:

This is the default scanning mode. It is optimized for detecting a single barcode at a time.

```
//minumum code snippet comes here (TBD: Waiting for Stefan K)
```
<p align="left">
  <img src="https://scanbot.io/wp-content/uploads/2025/01/barcode-sdk-accordion1.png" width="45%" />
</p>

##### MULTI Scanning:

The barcode scanner can also be configured to scan multiple barcodes simultaneously without closing the scanning screen.

```
//minimum code snippet comes here (TBD: Waiting for Stefan K)
```

<p align="left">
  <img src="https://github.com/doo/scanbot-barcode-scanner-sdk-example-react-native/raw/master/.images/multi-scanning.png" width="50%" />
</p>

##### Find & Pick

Given one or more barcodes, the SDK visually highlights and scans the correct items for your users. It automatically selects the barcode with the right barcode value from your camera feed.

```
//minumum code snippet comes here (TBD: Waiting for Stefan K)
```
<p align="left">
  <img src="https://github.com/doo/scanbot-barcode-scanner-sdk-example-react-native/raw/master/.images/find-pick.png" width="50%" />
</p>

#### Configuration options

The Scanbot React Native Barcode Scanner SDK offers numerous configuration options:

* **Barcode Filters**: Apply filters by barcode type or content, with regex pattern support to capture only relevant barcodes. See our [API References](https://scanbotsdk.github.io/documentation/barcode-scanner-sdk/react-native/api-docs/index.html) for a full overview.


* [**AR Overlay**](https://docs.scanbot.io/barcode-scanner-sdk/react-native/barcode-scanner/ui-components/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#ar-overlay)**:** Optional feature providing real-time barcode highlighting, preview, and tap-to-select functionality. Recognized barcodes are highlighted with customizable frames and text.

* [**Barcode Parsers**](https://docs.scanbot.io/barcode-scanner-sdk/react-native/supported-barcodes/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#data-parsers): Extract structured information from 2D barcodes like QR and Data Matrix codes. These include parsers for documents such as driving licenses (AAMVA), boarding passes, medical certificates, SEPA forms, Swiss QR codes, and vCard business cards.

* [**Scanning barcodes from an image**](https://docs.scanbot.io/barcode-scanner-sdk/react-native/barcode-scanner/detection-on-the-image/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites): Detect barcodes from still images in JPG or other formats, with support for single and multi-image detection.

#### **UI customization**

Customize the UI to match your app's look and feel.

> 💡Please refer to our [documentation](https://docs.scanbot.io/barcode-scanner-sdk/react-native/barcode-scanner/ui-components/?utm_source=npmjs.com&utm_medium=referral&utm_campaign=dev_sites#change-the-visuals-to-suit-your-needs) for a full overview of the visual configuration options.

##### **Configuring UI Elements:**

Tailor interface elements with custom text guidance, enable or disable the Top Bar with color modifications, or configure the Action Bar with features like Flashlight and Zoom buttons.

```
// Example code snippet comes here (TBD: Waiting for Stefan K)
// User Guidance
// Top Bar
// Action Bar
```

##### **Palette:**

Configure your UI's color palette to match your brand design for a cohesive user experience.

```
//minumum code snippet comes here (TBD: Waiting for Stefan K)
```

##### **Localisation:**

Easily localize strings displayed on buttons, labels, and text fields.

```
//minumum code snippet comes here (TBD: Waiting for Stefan K)
```

## Additional information

### Trial license

The Scanbot SDK examples will run for one minute per session without a license. After that, all functionalities and UI components will stop working. 

To try the React Native Barcode Scanner SDK without the one-minute limit, you can request a free, no-strings-attached 7-day trial license.

Our pricing model is simple: Unlimited barcode scanning for a flat annual license fee, full support included. There are no tiers, usage charges, or extra fees. Contact our team to receive your quote.

### Free developer support

Need help integrating or testing our Barcode Scanner SDK in your React Native project? We offer free developer support via Slack, MS Teams, or email.

As a customer, you also get access to a dedicated support Slack or Microsoft Teams channel to talk directly to your Customer Success Manager and our engineers.
