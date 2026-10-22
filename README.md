# Captur Demo for iOS

A SwiftUI app showing how to use CapturSDK to check e-bike parking, e-scooter parking, and package deliveries from photos.

## Requirements

- Xcode
- A GitLab token from Captur to install the SDK
- A Captur API key
- An iPhone running iOS 15.0 or later to use the camera

## Getting started

1. Open `CapturDemo.xcodeproj` in Xcode.
2. Use the GitLab username and token provided by Captur when installing the package. The project is configured to use CapturSDK 1.0.0.
3. Replace `<YOUR_CAPTUR_API_KEY>` in `CapturDemo/CapturDemoModel.swift` with your Captur API key.
4. Set your development team and a unique bundle identifier under **Signing & Capabilities** for the `CapturDemo` target.
5. Select your iPhone and run the `CapturDemo` scheme.

For CI, you can add the GitLab username and token to `~/.netrc` for `gitlab.captur.ai`.

## Demo flow

1. **Pick a use case** — Choose e-bike parking, e-scooter parking, or package delivery. Each use case has its own checks.
2. **Prepare a session** — Tap **Prepare Session** and wait for it to load. This gets Captur ready for the selected use case.
3. **Open the camera** — Tap **Open Camera** and allow camera access when prompted. Captur provides live guidance as you frame the photo.
4. **Capture a photo** — Use the live feedback to frame the photo, then tap the shutter or let the app capture automatically. Captur assesses the captured image.
5. **Review the result** — View the photo and decision. Tap **Retake** to try again or **New Session** to start over. The decision summarises the check.

The SDK integration is in `CapturDemo/CapturDemoModel.swift`. The use cases and sample locations are in `CapturDemo/UseCase.swift`.

See the [Captur iOS implementation guide](https://docs.captur.ai/ios/implementation/) for SDK documentation.
