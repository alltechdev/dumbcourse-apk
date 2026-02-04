## Dumbcourse App

Android app for [Dumbcourse](https://github.com/TripleU613/dumbcourse) forums with D-Pad navigation support and push notifications (ntfy).

## About

This app is a WebView wrapper for [Dumbcourse](https://github.com/TripleU613/dumbcourse) — a minimal, fast UI for Discourse built without modern JavaScript. It runs on everything from old devices to new flagships.

## Compatibility

Supports Android 6.0+ and Chrome WebView 44+.

## Configuration

**Package name** in `app/build.gradle`:
```gradle
namespace 'com.example.yourapp'
applicationId "com.example.yourapp"
```

**Package path** - rename `app/src/main/java/com/example/yourapp/` to match your package, and update `package` declarations in Java files.

**App icon** - replace `app/src/main/res/mipmap-*/ic_launcher.png` (sizes: mdpi 48px, hdpi 72px, xhdpi 96px, xxhdpi 144px, xxxhdpi 192px).

**App name** in `app/src/main/res/values/strings.xml`:
```xml
<string name="app_name">Your App Name</string>
```

**Forum URL** in `MainActivity.java`:
```java
private static final String BASE_URL = "https://YOUR_FORUM_URL_HERE";
```

**Notification title** in `NtfyService.java`:
```java
.setContentTitle("Forum Name")
title = "Forum Name";
```

## Build

```
./gradlew assembleRelease
```

## License

GPL-3.0
