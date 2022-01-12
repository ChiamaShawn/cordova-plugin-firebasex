cordova-ionicv5-firebase-x 


========================


This fix is based on https://github.com/dpa99c/cordova-plugin-firebasex work.

Brings push notifications, analytics, event tracking, crash reporting and more from Google Firebase to your Cordova project.

Supported platforms: Android and iOS

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**


# Installation
Install the plugin by:

```
npm install cordova-ionicv5-firebase-x
```


Copy the following statements

```
apply plugin: com.google.firebase.crashlytics
android {
     buildTypes {
         debug {
             firebaseCrashlytics {
                 mappingFileUploadEnabled false
             }
         }
         release {
             firebaseCrashlytics {
                 nativeSymbolUploadEnabled true
                 unstrippedNativeLibsDir "obj/local"
                 strippedNativeLibsDir "build/intermediates/jniLibs/release"
             }
         }
     }
 }
```

Paste them to the project level capacitor.build.gradle under the

```
apply from: "../../node_modules/cordova-plugin-firebasex/src/android/build.gradle"
```
statement

In the project level build.gradle file add the following classpath
```
classpath 'com.google.firebase:firebase-crashlytics-gradle:2.7.1'
```
