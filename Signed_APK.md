Alternative way to generate signed APK on Android project built with React Native


1) Bundle react-native assets into android project file
```
react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/<your-package-name>/src/main/assets/index.android.bundle --assets-dest android/<your-package-name>/src/main/res/
```
In case of `ENOENT: no such file or directory, open 'android/<your-package-name>/src/main/assets/index.android.bundle'` error, please run:
```
mkdir android/<your-package-name>/src/main/assets
```
2) Open android folder using Android Studio and generate signed apk from the `Build` menu
3) Install generated APK using:
```
- emulator ( -r switch will replace existing application) : adb -e install -r <path_to_signed_apk>
- USB device ( -r switch will replace existing application) : adb -d install -r <path_to_signed_apk>
- list all connected devices : adb devices -l
```
