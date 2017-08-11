Alternative way to generate signed APK on Android project built with React Native


1) Bundle react-native assets into android project file
```
react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/<your-package-name>/src/main/assets/index.android.bundle --assets-dest android/<your-package-name>/src/main/res/
```
2) Open android folder using Android Studio and generate signed apk from the `Build` menu
