# Farm Memory AI – Smart Farming Assistant (Android Kotlin + Jetpack Compose + Room)

A beginner-friendly, 100% offline-first Android application built for Indian farmers using **Kotlin**, **Jetpack Compose (Material 3)**, and **Room SQLite Database**. No login, no paid APIs, and no internet connection required to save or inspect records.

## Features Included

1. **Farmer Profile** (`ProfileScreen.kt`): Save farmer name, village, district, total land area (acres), soil type, and switch instantly between **English**, **हिन्दी**, and **मराठी**.
2. **Crop Memory** (`CropMemoryScreen.kt`): Record previous and current crops, Kharif/Rabi/Zaid seasons, sowing & harvesting dates, and production in quintals with Add/Edit/Delete.
3. **Soil Memory** (`SoilMemoryScreen.kt`): Store soil test reports (pH, Nitrogen, Phosphorus, Potassium in kg/ha, Organic Carbon %, lab name) with full edit/delete history.
4. **Expense Tracker** (`ExpenseTrackerScreen.kt`): Track Seed, Fertilizer, Pesticide, Labour, and Irrigation expenses in ₹ with automatic category & grand totals.
5. **Farming Activity Diary** (`ActivityDiaryScreen.kt`): Log Watering, Fertilizer, Spraying, Harvesting, and Weeding activities with notes and local phone gallery photos (`PickVisualMedia` + Coil).
6. **AI Farming Assistant** (`AiAssistantScreen.kt` + `OfflineAgronomyEngine.kt`): Analyzes the farmer's actual Room database history (soil type, crop rotation, latest NPK/pH report, and expenses) completely offline without inventing soil reports or guaranteeing yields.
7. **Farm History Dashboard** (`DashboardScreen.kt`): Shows total production, total expenses, season-over-season yield comparison bars, and recent farm activities.

## How to Build the Installable APK

### Option A: Android Studio (Recommended)
1. Open **Android Studio** (Ladybug 2024.2 or newer).
2. Click **Open** and select the `android-app` folder.
3. Wait for Gradle Sync to download AndroidX, Compose, and Room dependencies.
4. Click **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Your installable APK will be generated at:
   `app/build/outputs/apk/debug/app-debug.apk`

### Option B: Command Line (with Android SDK & Gradle installed)
```bash
cd android-app
gradle assembleDebug
```
Install on a connected Android phone via USB debugging:
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```
