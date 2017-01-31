# HelloKotlin

A "Hello World" Android APK that uses Kotlin instead of Java.

From the command line, do something like this to make sure that repository is in working order.

```sh
./gradlew --refresh-dependencies
./gradlew test
./gradlew clean check build
```

From the command line, the following can be used to build the APK, install it on a device and start the MainActivity.

```sh
./gradlew assembleDebug installDebug
PACKAGE_NAME=$(cat app/src/main/AndroidManifest.xml | grep package | sed 's/">.*$//' | sed 's/^.*"//')
ACTIVITY_NAME=".MainActivity"
adb shell am start -n "${PACKAGE_NAME}/${ACTIVITY_NAME}"
```

