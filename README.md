# StaySathi Android Tablet App — starter project

A responsive Hindi/English Android app shell with an original StaySathi brand and a hotel marketplace UI prototype.

## What is included
- Android Studio project (Kotlin Activity + WebView loading local assets)
- Tablet-responsive UI that also adapts to mobile widths
- Hindi/English language switch
- Sample hotel cards, search, category filters, favourites interaction
- Hotel detail dialog and demo booking request flow
- Demo host/property enquiry form
- No API keys or external services required to preview the UI

## Important limitations
This is a **working UI prototype**, not a production booking marketplace. Hotel names, ratings, prices and amenities are sample data. Booking requests and host enquiries are stored locally on the device only. Login/OTP, real availability, secure customer accounts, payments/refunds, property-owner dashboard, moderation, notifications, and server database are not connected. Do not accept real customer payments or promise real reservations using this prototype.

## Build an APK in Android Studio
1. Install Android Studio (recent stable version) and a compatible JDK (Android Studio's bundled JDK is fine).
2. Open this folder as an existing Android Studio project.
3. Let Gradle sync. Android Gradle Plugin 8.7.3 requires a compatible Gradle 8.9+ distribution; Android Studio may offer to download it.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK is typically created at `app/build/outputs/apk/debug/app-debug.apk`.

This source package does not include a compiled APK because APK compilation requires the Android/Gradle build toolchain. Build the APK using the steps above.

## Suggested production architecture
- Android app: Kotlin + Jetpack Compose or this WebView shell
- Backend API: authenticated REST API
- Database: PostgreSQL
- Auth: phone OTP provider with rate limits and abuse protection
- Payments: RBI-compliant payment gateway integration; do not store card details
- Property onboarding: identity/business verification, room inventory, rate plans
- Booking state machine: hold -> payment pending -> confirmed/failed -> cancelled/refunded
- Admin portal: property approval, dispute handling, audit logs
- Privacy: consent, retention/deletion, secure transport, access control, Indian legal/privacy compliance

## Project identity
- App name: StaySathi
- Application ID: `com.staysathi.app`
- Version: `0.1.0`
- Min Android SDK: 23
