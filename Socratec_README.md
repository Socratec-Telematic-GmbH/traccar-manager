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

1. Resolve dependencies by running `flutter pub get`. The command is used in Flutter projects to fetch and install the dependencies listed in the `pubspec.yaml` file. It ensures that all the required packages and their versions are downloaded and made available for the project.
1. If required generate platform specific app bundles by running:
```
flutter build ios
flutter build apk
```