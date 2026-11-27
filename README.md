# Islamic Life 2.1

Islamic Life is a Bengali-first Islamic life and learning PWA with an Android build workflow.

## Included
- Full 114-surah Quran reader through QuranEnc API, Arabic text and Bengali translation. Surahs viewed are cached locally; use the in-app download-all control to cache all 114 on that device. First download requires internet.
- 99 Asma-ul-Husna entries with Arabic, Bengali pronunciation and meaning.
- Prayer time calculation and Qibla direction; GPS coordinates or manual coordinates can be saved.
- Location profile fields: division, district, upazila/thana, union and village.
- Bengali, Gregorian and Hijri date display. Hijri date may differ from Bangladesh moon-sighting announcements.
- Madrasa tools: student register, attendance, exam marks, results, teacher list, class routine, notices, fee records and summary reports.
- Decorative subtle Islamic geometric background, responsive PWA layout.

## Deploy web app
1. Extract this ZIP.
2. Upload **all files and folders**, including the hidden `.github` folder, to the repository root.
3. Commit to `main`.
4. In GitHub: Settings → Pages → Build and deployment → Source: GitHub Actions.
5. Open Actions and wait for `Deploy Islamic Life to GitHub Pages` to succeed.

## Build Android APK
1. Ensure `.github/workflows/android-apk.yml` exists in the repository.
2. Push/commit to `main`, or open Actions → Android APK Build → Run workflow.
3. Wait for a green check.
4. Open the successful run → Artifacts → `islamic-life-debug-apk`.
5. Download and extract the ZIP to get `app-debug.apk`.

This is a debug APK for testing, not a Play Store signed release. A production release requires signing configuration and release build steps.

## Important limitations
- Prayer times depend on correct coordinates and calculation assumptions. Verify with the local mosque; calculation settings may need adjustment for local convention.
- GPS reverse lookup is best-effort and uses OpenStreetMap Nominatim. If a local administrative label is missing, edit the location fields manually.
- Madrasa records in this version are stored only in the current browser/device using local storage. They are not synced between users or devices. Do not store sensitive student data in this prototype. Multi-user access requires a secure backend, authentication, authorization and privacy controls.
- Calendar display uses a calculated Bangla date and the browser's Umm al-Qura Hijri calendar. Local moon-sighting dates can differ.

## Design update
- Refreshed the interface with a modern emerald, ivory and gold visual theme.
- Applied SolaimanLipi for Bengali UI text, Amiri for Quranic Arabic display, and Noto Naskh Arabic for general Arabic text.
- Updated the developer profile page using the supplied education and work details; omitted unverified contact information.
