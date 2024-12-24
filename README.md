# Expo Camera Preview Freeze/Corruption Bug

This repository demonstrates a bug in the Expo Camera API where the camera preview may freeze or become corrupted after extended use or multiple photo captures.  The issue is more pronounced on devices with lower processing power.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using Expo Go or a similar Expo client.
4. Take multiple photos consecutively or leave the camera app running for an extended period.  Observe the camera preview for freezing or corruption.

## Bug Solution

The proposed solution involves implementing a mechanism to reset the camera preview periodically or after a specific number of captures. This prevents resource exhaustion or internal state errors within the Expo Camera API that may lead to the freezing or corruption. This is achieved by using the `Camera.stopPreview` and `Camera.startPreview` methods in a controlled manner.