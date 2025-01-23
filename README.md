# Expo CLI Android Build Failure: AGP Version Conflict

This repository demonstrates a rare Expo CLI build issue on Android, stemming from conflicts or incompatibilities with the Android Gradle Plugin (AGP) version.

## Problem:

Building an Android APK using `expo build:android` results in a Gradle build failure.  Error messages may indicate missing or mismatched AGP methods.

## Solution:

The solution involves carefully examining your project's `gradle` files and ensuring compatibility between the AGP version, Gradle version, and other dependencies.  Often, updating or downgrading specific versions resolves the issue.

## Reproduction Steps (bug.js):

1. Create a new Expo project (this file won't fully reproduce the error since it depends on specific dependency versions).
2. Introduce deliberate conflicts in the Gradle configuration (e.g., incompatible AGP and Gradle versions).
3. Attempt to build the Android project using `expo build:android`.  The build should fail.   

## Solution (bugSolution.js):

1. Check `android/build.gradle`, `android/app/build.gradle`, and `gradle/wrapper/gradle-wrapper.properties` for version compatibility between Gradle, AGP, and other dependencies.
2. Update these files to ensure all versions are compatible according to the Expo documentation and the AGP release notes.
3. Clean and rebuild the project.

