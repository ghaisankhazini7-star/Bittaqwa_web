# Bittaqwa

**Bittaqwa** is an Islamic application developed using **Flutter**. This project offers several features to help users access daily prayers (duas), view prayer schedules, watch Islamic study videos, and calculate *zakat* (obligatory alms).

> **Important — there are two different versions of Bittaqwa:**
> - **Flutter App (source project):** The application project containing Dart code and platform configurations for Android and iOS. This is the primary project for development and building the application.
> - **Web Preview:** A Flutter Web version that runs in a browser. The Netlify preview can be displayed within an iPhone 16 frame for demonstration purposes. This frame is merely a visual mockup; it is **not** a native iOS application or an iPhone simulator.

---

## Demo

- **Web Preview:** [Open Bittaqwa Web Preview](https://YOUR-NETLIFY-SITE.netlify.app)
- **GitHub Repository:** [Bittaqwa](https://github.com/YOUR-USERNAME/YOUR-REPOSITORY)

> Replace the example URLs above with your own Netlify link and GitHub repository link.

---

## Features

- **Dashboard:** The main page serving as a navigation hub for Bittaqwa’s features.
- **Prayers (Duas):** A categorized list of prayers with detailed views for each.
- **Prayer Schedules:** Displays prayer times using an external data service/API.
- **Islamic Study Videos:** A list of YouTube-based study videos with an integrated video player.
- **Zakat Calculator:** Helps estimate *zakat* based on the total value of assets provided.

Accessing prayer schedules and playing videos requires an internet connection. Additionally, some videos may not be playable via embed if the video owner or YouTube has restricted playback on external websites.

---

## Flutter App vs. Web Preview

| | Flutter App (Main Application) | Web Preview (Website/Demo) |
|---|---|---|
| Format | Flutter project with Dart source code | A Flutter Web build served via a browser |
| How to access | Run/built via Flutter on supported platforms | Accessed via a Netlify link or a web browser |
| Main folders | `lib/`, `android/`, `ios/`, `pubspec.yaml`, and other platform-specific folders | `build/web/` |
| Purpose | Development and building of the application for various devices | A demo allowing users to try out Bittaqwa without needing to set up a Flutter project |
| iPhone 16 frame | Not required for a native application | Optional; serves as an HTML/CSS mockup to frame the Web Preview |

### 1. Flutter App — the actual application project

The Flutter project folder contains the core source code for Bittaqwa. The user interface and features are written in Dart within the `lib/` folder. The project also includes platform-specific folders such as `android/`, `ios/`, `web/`, `macos/`, `windows/`, and `linux/`.

These platform folders serve as configuration/build targets for Flutter. Successfully running or releasing the application on any given platform depends on the relevant SDKs, toolchains, configurations, and testing for that specific platform.

Example of running the application on an emulator or a device detected by Flutter:

```bash
flutter doctor
flutter pub get
flutter devices
flutter run -d <device-id>
```

Example of creating an Android build:

```bash
flutter build apk --release
```

Example of creating an iOS build (requires macOS and Xcode):

```bash
flutter build ios --release
```

The build commands do not automatically publish the application to the Google Play Store or the App Store. Processes such as code signing, store configuration, and meeting publication requirements are still necessary.

### 2. Web Preview — a version accessible via a website

The Web Preview is the result of compiling the Flutter project for a web browser. Users can access the website via Chrome, Safari, or any other modern browser without needing to run Flutter on their own computers. To generate a Web build from the project source:

```bash
flutter pub get
flutter build web --release
```

The build output will be created in:

```text
build/web/
```

**To deploy a Web Preview without an iPhone frame**, upload the `build/web/` folder to a static hosting service such as Netlify.

### 3. Web Preview with an iPhone 16 frame

The demo version featuring an iPhone 16 frame uses an HTML/CSS page as a wrapper. This page displays the Flutter Web output within the screen area using an `iframe`.

Therefore:

- The application running inside the frame remains a **Flutter Web** app.
- The iPhone 16 frame is merely a presentation element/mockup on the website.
- The frame is not an iOS emulator, not an actual iPhone device, and not an `.ipa` application file.
- To run a native application on an iPhone, use the Flutter project and run/build it via Xcode on an iOS device or simulator.

If you are using the Netlify iPhone 16 package—which contains an `index.html` file and an `app/` folder—upload the **outermost folder** that contains both of them. Do not upload only the `app/` folder.

Structure of the iPhone 16 preview package:

```text
Bittaqwa_iPhone16_Netlify/
├── index.html   # iPhone 16 mockup/frame page
└── app/         # Flutter Web build output
├── index.html
├── flutter_bootstrap.js
├── main.dart.js
└── assets/
```

---

## Technologies

- **Flutter & Dart** — framework and language
