# FrameX TV Android app

A minimal Android TV WebView wrapper for `https://framextv.cc/`.

## Features
- Landscape, immersive full-screen display
- Android TV / Google TV launcher entry
- JavaScript and DOM storage enabled for site functionality
- D-pad/remote interaction through the WebView
- Android Back button navigates WebView history
- HTTPS-only top-level navigation; mixed content is disabled

## Build the APK
1. Install Android Studio (current stable) with Android SDK Platform 35 and JDK 17.
2. Open this folder in Android Studio.
3. Allow Gradle sync to complete.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Find the debug APK at `app/build/outputs/apk/debug/app-debug.apk`.

Or, with a compatible Gradle installation:
```bash
gradle assembleDebug
```

## Important
This project is a WebView shell, not an offline copy of the website. It requires internet access.
The site content and playback compatibility depend on the website itself and Android System WebView.
The site could not be inspected for full functionality during project generation. Review the domain and
site permissions before installing or distributing the APK. No login credentials or site data are
embedded in this project.


## Build without installing Android Studio (GitHub Actions)
1. Create a new GitHub repository and upload the contents of this project.
2. Open the repository's **Actions** tab.
3. Select **Build FrameX TV APK** and click **Run workflow** (or push to `main`).
4. When the run finishes, open it and download the **FrameX-TV-debug-apk** artifact.
5. Extract the downloaded artifact to get `app-debug.apk`.
