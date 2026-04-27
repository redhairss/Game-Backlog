# Game Backlog Tracker — Android App

A WebView-based Android app wrapping your personal Steam game backlog tracker.

---

## What You Need (all free)

1. **Android Studio** — https://developer.android.com/studio
2. **Java JDK 11+** (bundled with Android Studio)
3. Your Android phone with **USB debugging enabled**

---

## Step 1 — Install Android Studio

1. Download Android Studio from https://developer.android.com/studio
2. Run the installer and follow the setup wizard
3. When prompted, install the **Android SDK** (default options are fine)
4. Let it finish — this may take 10–15 minutes on first run

---

## Step 2 — Open This Project

1. Open Android Studio
2. Click **"Open"** (or File → Open)
3. Navigate to this `GameBacklog` folder and select it
4. Click **OK** — Android Studio will sync the project (takes a minute)
5. If prompted to upgrade Gradle, click **"Don't remind me again"** or just accept

---

## Step 3 — Enable USB Debugging on Your Phone

1. Go to **Settings → About Phone**
2. Tap **"Build Number"** 7 times until it says "You are now a developer"
3. Go to **Settings → Developer Options**
4. Turn on **"USB Debugging"**
5. Connect your phone to your PC via USB
6. On your phone, tap **"Allow"** when it asks about USB debugging

---

## Step 4 — Run the App

1. In Android Studio, your phone should appear in the device dropdown at the top (e.g. "Galaxy S23")
2. Click the green **▶ Run** button (or press Shift+F10)
3. Android Studio will build and install the app on your phone
4. The app will launch automatically!

---

## Step 5 — Build a standalone APK (optional, to share or sideload)

1. In Android Studio: **Build → Build Bundle(s) / APK(s) → Build APK(s)**
2. Wait for it to finish — a notification will appear at the bottom
3. Click **"locate"** in the notification to find your APK
4. The APK will be at: `app/build/outputs/apk/debug/app-debug.apk`
5. Copy this to your phone and install it (you may need to allow "Install from unknown sources" in Settings)

---

## Project Structure

```
GameBacklog/
├── app/
│   ├── src/main/
│   │   ├── assets/
│   │   │   └── index.html          ← Your entire backlog app lives here
│   │   ├── java/com/redhairss/gamebacklog/
│   │   │   └── MainActivity.java   ← Android WebView wrapper
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml
│   │   │   ├── mipmap-*/           ← App icons
│   │   │   └── values/
│   │   │       ├── strings.xml
│   │   │       ├── colors.xml
│   │   │       └── themes.xml
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md
```

---

## Updating Your Game List

To update your game list or change anything in the app:
1. Edit `app/src/main/assets/index.html`
2. Re-run the app from Android Studio (Step 4)

---

## Troubleshooting

**"SDK not found"** → Open Android Studio → SDK Manager → Install Android SDK 34

**Phone not showing up** → Make sure USB debugging is on, try a different USB cable

**App crashes on launch** → Check Logcat in Android Studio for errors

**Gradle sync fails** → File → Invalidate Caches → Restart
