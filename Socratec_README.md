# [Traccar Manager app](https://www.traccar.org/manager)

## Overview

Traccar Manager is the official mobile app for managing and monitoring your GPS tracking devices with the open-source Traccar platform.

- **Live Tracking**: View the real-time location of all your devices on an interactive map.
- **Device Management**: Add, edit, or remove devices directly from your mobile device.
- **Event Notifications**: Receive alerts for geofence crossings, device status changes, and more.
- **History and Reports**: Review past routes and generate trip history for any device.
- **Secure and Private**: All your data stays on your own server—no third-party access.

Connect the app to your Traccar Server, log in with your credentials, and instantly manage and monitor your fleet or personal devices from anywhere.

## Local Setup

1. Make sure Dart and Flutter SDK is installed. This can be done by following this guide https://docs.flutter.dev/get-started/quick. 
1. Resolve dependencies by running:
```
flutter pub get
```
The command is used in Flutter projects to fetch and install the dependencies listed in the `pubspec.yaml` file. It ensures that all the required packages and their versions are downloaded and made available for the project.
1. To generate platform specific app bundles run:
```
flutter build ios
flutter build apk
```
For iOS CocoaPods is required to resolve dependencies. If not installed, run
```
gem install cocoapods
```

## Brand Mobile Apps to Socratec
The provided Flutter App from Traccar can be branded using a script. The script customizes the Traccar Manager app to create a company-specific branded version for Socratec.
The script automates the following tasks:

1. Generate App Icons:
Deletes existing app icons and regenerates platform-specific icons (Android and iOS) using a provided logo file.
1. Update App Name:
Updates the app's name in the Android and iOS configuration files.
1. Update Package ID/Bundle identifier:
Changes the Android applicationId and iOS PRODUCT_BUNDLE_IDENTIFIER to the specified package ID.
1. Update App Version:
Updates the app version in the pubspec.yaml file.
1. Update Server URL:
Replaces the default server URL in the app's code with a custom URL.
1. Create Android Keystore:
Generates a new keystore for signing the Android app and updates the Gradle configuration.

### Run branding script
The branding can be triggered using this command 
```
dart tool/socratec_branding.dart
```
After script finished, verify that the app's branding (name, icons, etc.) has been updated.
Run the following commands to ensure everything is set up correctly:
```
flutter clean
flutter pub get
flutter build apk
flutter build ios
```