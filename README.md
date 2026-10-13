# Revision Hub (Android app)

## Easiest: build online (no Android Studio)
1. Create a new GitHub repo and push this whole folder to it.
2. Open the repo > Actions > "Build APK" > wait ~5 min.
3. Open the finished run > Artifacts > download `revision-hub-apk` (zip) > extract `app-debug.apk`.
4. Copy the APK to your phone and install (allow "Install unknown apps").

## Or build locally (needs Node 20, Java 17, Android Studio)
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
APK path: android/app/build/outputs/apk/debug/app-debug.apk

## Editing the app
All UI lives in www/index.html. After changes: push again (online build) or run `npx cap sync android`.
