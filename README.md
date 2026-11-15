# Project Interlink

Native Android Studio project built with Kotlin and Jetpack Compose.

## Source project

The complete Android Studio source is stored in `ProjectInterlink-source.zip.base64` at the repository root. Reconstruct it locally with:

```bash
base64 --decode ProjectInterlink-source.zip.base64 > project.zip
unzip project.zip
```

Open the extracted `ProjectInterlink` folder in Android Studio.

## Build

The GitHub Actions workflow in `.github/workflows/android.yml` reconstructs the project, installs Android SDK 35, and runs:

```bash
gradle -p ProjectInterlink assembleDebug
```

On a successful run, download the `project-interlink-debug-apk` artifact from the Actions run page.

## Firebase

The Android Firebase client configuration is at `ProjectInterlink/app/google-services.json` inside the archive. The app uses Firebase SDK dependencies, but the current app README/source describes this as a UI/demo foundation; do not assume account authentication or remote messaging is live until those flows and Firebase rules/functions are implemented and tested.

## Current build scope

This workflow creates a debug APK for installation/testing. It is not a signed Play Store release.
