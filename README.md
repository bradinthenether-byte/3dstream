# Mupen64Plus-AE for Android

This workspace contains the open-source Mupen64Plus Android Edition (AE), an
Android frontend and N64 emulator based on the Mupen64Plus project. It supports
loading games from files selected by the user; no commercial game ROMs are
provided.

This is the upstream Mupen64Plus-AE project, not a new emulator implementation.
Upstream source and project information:

- Repository: <https://github.com/mupen64plus-ae/mupen64plus-ae>
- Upstream license: GPL-3.0, included in [`gpl-license`](./gpl-license)
- Emulator source and third-party notices are included in their respective
  project directories.

## Build a debug APK

Install Android Studio with Android SDK Platform 36 and NDK `26.1.10909125`.
The project uses Java 17 and includes a Gradle wrapper. From this directory,
run:

```sh
./gradlew :app:assembleDebug
```

The APK is written to `app/build/outputs/apk/debug/Mupen64PlusAE-debug.apk`.
The app's debug package ID has a `.debug` suffix. Alternatively, open this
directory in Android Studio and run the `app` configuration on an Android
device.

## Use

Install the APK, open the app, and add or scan for N64 ROM files stored on your
device. ROM files remain user-provided; this project does not convert ROMs into
Android applications. Only load games you are legally authorized to use.

The emulator includes built-in fast, balanced, and accuracy-focused graphics
profiles, per-game overrides, and separate controls for display, shaders,
audio, touchscreen, and physical controllers. The default profile is
GLideN64-Medium on devices that support it, balancing visual quality and
performance; change it in **Profiles > Select Profiles** or choose a profile
for an individual game. Actual speed and compatibility vary by device and game.

## Upstream build guidance

See the upstream [README](https://github.com/mupen64plus-ae/mupen64plus-ae#readme)
and [license](https://github.com/mupen64plus-ae/mupen64plus-ae/blob/master/gpl-license)
for project details and licensing terms.
