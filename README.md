# Maverick OCR (Automated Product Information Extractor)
Native Android OCR mobile application purpose-built as an automated extraction solution replacing manual data entry for the **GDSS-Maverick Hackathon**.

The app is runs 100% on-device and completely offline, guaranteeing high enterprise-grade security, lightning-fast response times, and resilience against network latency.

## Key Features
1. **Onboarding Walkthrough**: A modern, 3-screen slideshow welcoming evaluators with hackathon branding, professional photography tips, and core functionality summaries.
2. **Double-Confirmation Camera Capture**: Integrates seamlessly with the device's native camera using modern Compose launchers. Captures high-res photos and prompts users for validation before initiating OCR, preventing accidental execution.
3. **Advanced Contrast Preprocessing**: Applies automated image preprocessing filters (grayscale conversion, custom contrast magnification, upscaling under 800px width, and downsampling over 1280px) to enhance low-light labels and perspective angles.
4. **On-Device ML Kit OCR**: Implements Google's on-device ML Kit Text Recognition to process scans on background threads, complete with shimmering feedback.
5. **Smart Field Identification**: Scans extracted strings automatically with custom regex logic to detect structures like Prices, Dates, Emails, and Phone Numbers, displaying them on colored highlight chips.
6. **Voice Synthesis (TTS)**: Life-like vocal feedback summarizing scan results and structural coordinates.
7. **Local Persistence (Room)**: Secure SQLite offline caching of previous scans, including previews, counts, and metadata.
8. **Swipe-to-Delete & Multi-Select**: Effortlessly manage cache lists with modern, responsive gestures.
9. **Interactive Verification Workspace**: Loaded history cards are restored back to the scanning home screen upon tapping, enabling instant review and side-by-side preprocessed contrast comparison.
10. **Data Export Choices**: Export all historic logs directly as Microsoft Excel/Google Sheets compliant CSV tables or formatted JSON databases.
11. **Shake Device Reset**: Shake the device anytime while reviewing results to instantly reset and launch the camera workspace.
12. **Milestones & Streak Gamification**: Dynamic day-to-day scanning streak tracking and progress indicators for unlocks (First Scan, Text Detective, OCR Master, 100 Club).

---

## Build Requirements
- **Integrated Development Environment (IDE)**: Android Studio Ladybug (2024.2.1) or newer.
- **Gradle Version**: 8.7+ (runs Kotlin DSL).
- **Minimum SDK Level**: Android API 24 (Android 7.0 Nougat) for robust device coverage.
- **Compile & Target SDK Level**: Android API 36.
- **Language Stack**: 100% Kotlin & Jetpack Compose.

---

## Core Dependencies & Libraries Used
- **Jetpack Compose**: Standard modern Material 3 UI design engine.
- **Google ML Kit Text Recognition v2**: High-performance, dynamic on-device character OCR engine.
- **CameraX API Suite**: Seamless capturing interface wrapper.
- **Coil Compose Image Loader**: Lightweight asynchronous image loader pipeline.
- **Room Persistence Library**: Reactive, offline-first SQL database persistence.
- **Kotlin Coroutines & Flow**: Concurrent reactive operations running completely on background threads.
- **Robolectric & Roborazzi**: Local JVM tests and visual screenshot comparison runner.

---

## Setup & Setup Guides
1. **Clone the Project**: Download and unzip the package or pull directly from the submission repository.
2. **Open in Android Studio**: Launch Android Studio, click **File > Open**, and select the project root directory.
3. **Gradle Sync**: Let the IDE fetch play-services, Room, and Compose libraries from Maven Central.
4. **Run Project**: Connect an Android device (via USB/Wi-Fi debugging) or launch a virtual device AVD, and click the **Run** green arrow.

---

## APK Generation Instructions
To compile and generate a standalone distributable release-ready APK:
1. Navigate to the top menu and select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
2. Android Studio will run the compiler. Once finished, a notification popup will appear at the bottom right.
3. Click **Locate** on the popup, or navigate directly to `/app/build/outputs/apk/debug/` to find your runnable `app-debug.apk` file!
