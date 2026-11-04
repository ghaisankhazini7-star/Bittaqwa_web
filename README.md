Application programming language.
- **Material Design** — Flutter interface components.
- **HTTP** — communication with data services/prayer time APIs.
- **Intl** — number and currency formatting.
- **YouTube Player package** — integration of a YouTube video player for religious study (kajian) content, as per the dependencies used in the project.
- **Netlify** — hosting for Web Preview.

Specific dependency versions can be found in the `pubspec.yaml` and `pubspec.lock` files within the repository.

---

## Project Structure

```text
bittaqwa_Ghaisan/
├── android/                     # Android configuration
├── ios/                         # iOS configuration
├── web/                         # Flutter Web configuration
├── macos/                       # macOS configuration
├── windows/                     # Windows configuration
├── linux/                       # Linux configuration
├── assets/
│   ├── fonts/                   # Poppins fonts
│   └── image/                   # Application images and assets
├── lib/
│   ├── main.dart                # Application entry point
│   ├── data/                    # Prayer (doa) data
│   ├── models/                  # Data models
│   ├── presentation/
│   │   ├── screen/              # Dashboard and Zakat/prayer screens
│   │   └── widget/              # Reusable widgets
│   ├── screens/                 # Screens for prayers, prayer times, religious studies, and details
│   └── services/                # Services for data/API retrieval
├── test/                        # Unit/widget tests (if available)
├── pubspec.yaml                 # Project configuration and dependencies
└── README.md
```

---

## Running the Project Locally

### Requirements

- Flutter SDK (must meet the version constraints specified in `pubspec.yaml`).
- Dart SDK (included with Flutter).
- Visual Studio Code or Android Studio (optional, for use as an editor).
- Android SDK (for running/building on Android).
- Xcode (for running/building on iOS; requires macOS). Check your Flutter installation:

```bash
flutter --version
flutter doctor
```

### Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Fetch dependencies:

```bash
flutter pub get
```

Run in Chrome:

```bash
flutter run -d chrome
```

Run on a detected emulator/device:

```bash
flutter devices
flutter run -d <device-id>
```

---

## Deployment to Netlify

### A. Standard Web Preview Deployment

1. Build the Flutter Web app:

```bash
flutter build web --release
```

2. Locate the `build/web/` folder.
3. Upload the `build/web/` folder to Netlify Drop, or set this folder as the **publish directory** in your Netlify configuration.
4. Open the deployment URL to access Bittaqwa via your browser.

### B. Web Preview Deployment with an iPhone 16 Frame

1. Use the iPhone 16 preview package, which contains an `index.html` file and an `app/` folder.
2. Extract the ZIP package.
3. Ensure that `index.html` and the `app/` folder are located within the same directory.
4. Upload this root folder to Netlify.
5. Open the deployment URL. The main page will display the Flutter Web app inside an iPhone 16 mockup.

> Whenever the Flutter source code is updated, rebuild the Web version and update the contents of the `app/` folder within the preview package. Keep the `index.html` file (the iPhone 16 wrapper) unchanged.

---

## Notes

- The Web Preview is a way to test the browser-based version of Bittaqwa; its appearance may differ from the native application on a physical device.
- The iPhone 16 frame is merely a presentation mockup and does not indicate that the application is running on an actual iPhone.
- Features requiring an internet connection will not function correctly when the device is offline. - Ensure that API keys, tokens, passwords, and other secrets are not included in public repositories. Use environment variables or secret configuration features provided by your hosting service where necessary.
- Double-check the terms of use and embedding restrictions for each YouTube video.
- The Zakat calculation feature within the application serves as an estimation tool. Please verify the *nisab* (minimum threshold) and Zakat requirements with official sources or qualified authorities.

---

## Contributions

Suggestions, bug reports, and feature enhancements can be submitted via GitHub Issues or Pull Requests.

Before submitting any changes, please run the following basic checks:

```bash
flutter pub get
flutter analyze
flutter test
```

---

## License

The project license has not yet been defined. Do not assume that this source code is free to be reused or redistributed until the project owner adds a `LICENSE` file and specifies the terms.

---

**Built with Flutter for Bittaqwa.**
