# MarineWatch - get your APK in ~5 minutes (no Android Studio needed)

1. Create a free account at github.com, then click New repository (name: marine-watch).
2. Upload everything in this folder to the repo (drag the files in, including the
   hidden .github folder; or use git push).
3. Open the repo's Actions tab -> "Build APK" -> wait for the green tick.
4. Open that run -> Artifacts -> download "marine-watch-apk" -> unzip -> app-release.apk
5. Copy the APK to your phone and install (allow "install unknown apps").

Prefer building locally? Install Flutter, then run in this folder:
  flutter create --platforms=android --org com.marinewatch --project-name marine_watch .
  (add CAMERA / ACCESS_FINE_LOCATION / INTERNET permissions to android/app/src/main/AndroidManifest.xml)
  flutter pub get
  flutter build apk --release
APK: build/app/outputs/flutter-apk/app-release.apk

What works: camera-only capture + automatic GPS/timestamp (mock-location detected),
64-bit DCT perceptual-hash duplicate merge (100 m, Hamming <= 10), Trust Score with the
paper's three routing bands, reputation, eco-points, badges, impact board, explainable
per-report breakdown.
Demo mode: no trained classifier or backend yet, so AI confidence is a slider.
