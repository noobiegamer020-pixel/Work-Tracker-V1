# Field Day Planner – APK build

## Option A: Build in the cloud (no Android Studio needed)
1. Create a free GitHub repo and upload everything in this folder (keep the .github folder).
2. Go to Actions > "Build APK" > Run workflow.
3. When it finishes, download the artifact "FieldDayPlanner-apk" (contains app-debug.apk).
4. Copy it to your phone and install (allow "Install unknown apps").

## Option B: Build locally
Requires Node 18+, JDK 17, Android Studio (SDK).
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android      # then Build > Build APK(s)
or from the command line:
    cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Updating the app
Replace www/index.html, run `npx cap sync android`, rebuild.
