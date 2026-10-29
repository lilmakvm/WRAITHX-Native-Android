# WRAITHX Native Android Launcher — Starter Project

This is an Android Studio source project, not a prebuilt APK.

## What is included
- A native Kotlin Android home-screen activity registered as a HOME app.
- A horizontal-style launcher list of app shortcuts.
- A real dark/light appearance switch (black/white surfaces).
- A Control Center shortcut that calls Android's Quick Settings global action **only after the user enables the WRAITHX accessibility service**.
- A shortcut to Android system settings and the default Home app settings.

## Build
1. Open this folder in Android Studio (recent version).
2. Let Gradle sync and install the required Android SDK (compile SDK 35).
3. Build > Build APK(s), or run it on your Android phone.
4. Install the debug APK on your own device.

## First-run setup
1. Open WRAITHX.
2. Tap **Set WRAITHX as default Home app** and select WRAITHX.
3. To make Control Center open Android Quick Settings, open Android Accessibility settings and enable **WRAITHX Quick Settings**. Android requires this explicit user consent. Accessibility access is powerful; enable it only if you trust the app source.

## Important limitations
- This starter uses a small set of common package names for app shortcuts; manufacturers and app versions may use different package IDs.
- Android 11+ package visibility rules and Play Store policies may require declaring package visibility more narrowly or reviewing the QUERY_ALL_PACKAGES permission before public release.
- It has not been built or tested on a physical device in this environment. It is a starter project, not a Play Store-ready release.
- The web version hosted on AppDeploy remains separate; AppDeploy publishes web apps, not native Android APKs.
## Cloud build from a phone (GitHub Actions)
This project includes `.github/workflows/build-apk.yml`. After the project files are uploaded into a GitHub repository:
1. Open the repository's **Actions** tab.
2. Choose **Build WRAITHX APK** and tap **Run workflow** (or wait for the first push build).
3. Open the completed run and download the `WRAITHX-debug-APK` artifact.
4. Extract the artifact ZIP to get `app-debug.apk`, then open the APK on the Android phone to install it.

The debug APK is for testing, not Play Store release. Review the source and Android permissions before installing. This cloud workflow has not been run from this environment, so APK generation is not yet verified.
