# Mobihelp SDK for Android

This is a simple wrapper around the officially distributed code (https://github.com/freshdesk/mobihelp-android) that makes it easy to add the SDK to your App as a dependency (without all the hassle of checking the project out and adding it as a module).

To use this, add the jitpack maven repository to your build.gradle file:
```gradle
repositories {
    maven { url "https://jitpack.io" }
    ...
}
```
and add the dependency:
```gradle
dependencies {
    ...
    compile 'com.github.tinsukE:mobihelp-sdk-android:v1.4'
}
```
# Changes to the original
I felt compelled to make the following changes as an improvement to the original `AndroidManifest.xml`:
- Removed the `READ_LOGS permission` since it shows as "Device & app history" when installing from the Play Store (it sounds creepy and there is no real reason for Mobihelp to use it).
- Removed the `android:label` field from the `application` tag, since it would override the name you define for your App.
