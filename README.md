# Islamic Life 2.0 — Complete Ready-to-Upload Package

A Bengali-first Islamic lifestyle PWA with an Android (Capacitor) build workflow.

## Included now
- Emerald Premium responsive interface based on the supplied `islamic-life-updated-4.zip`.
- Full 114-surah Quran section. Arabic ayah text and Bengali translation are fetched from QuranEnc's public API, with per-surah IndexedDB caching and a button to cache all 114 surahs for offline use.
- 99 commonly enumerated Asma ul Husna with Arabic, Bengali pronunciation and concise Bengali meanings.
- Existing sections and tools from the supplied project are retained where possible.
- PWA manifest and service worker.
- GitHub Pages deployment workflow.
- GitHub Actions workflow that builds a debug Android APK using Capacitor and uploads it as an Actions artifact.

## Deploy the website
1. Extract this ZIP.
2. Open your existing GitHub repository `israfiltanim52-ship-it/islamic-life`.
3. Upload the **contents** of the extracted folder to the repository root (not the ZIP file itself), replacing old files when prompted.
4. Commit to the `main` branch.
5. In GitHub: Settings → Pages → Build and deployment → Source: **GitHub Actions**.
6. The workflow deploys the root website. Wait for the Pages workflow to finish.

## Build Android APK
After pushing to `main`, open the repository's **Actions** tab.
1. Select **Build Android APK**.
2. Wait for the workflow to complete.
3. Download the `islamic-life-debug-apk` artifact from the workflow run.
4. Extract the artifact to get `app-debug.apk`.

This is a debug APK for testing/sideloading. A Play Store release requires a separately managed signing key and release configuration. Never commit a signing key or passwords to GitHub.

## Quran data and translation
- Provider: QuranEnc API — https://quranenc.com/bn/home/api/
- The app discovers an available Bengali translation from the API at runtime; no API key is required according to its published API documentation.
- When a surah is opened, its complete ayah response is cached locally in IndexedDB. The Quran page includes an optional sequential “cache all 114 surahs” action.
- First-time Quran download requires internet. Previously cached surahs can then be read offline.
- QuranEnc recommends pairing Uthmani text with the matching Hafs 20 font/text package. The API's Bengali translation and text are served by QuranEnc; consult its current documentation and translation notes.
- QuranEnc API documentation: https://quranenc.com/bn/home/api/
- The app identifies the translator as Dr. Abu Bakr Muhammad Zakaria, the source as QuranEnc.com, and the translation release as V1.1.1 in the Quran section. QuranEnc terms require clear attribution, version information, transcript/source information, no modification of the translation, and keeping it updated with the source. No inappropriate advertisements should be shown alongside the translation.

## Asma ul Husna
The app includes a commonly used 99-name enumeration. Scholars note that the hadith affirming 99 names is authentic, while the exact enumerated list/order has scholarly discussion and variant lists. The app displays this caveat rather than presenting the enumeration as the only possible list.

## Important operational notes
- Prayer-time calculations and notification behavior must be tested on real devices and compared with local mosque timetables.
- Location access requires HTTPS and user permission.
- Web Push/alarms can be restricted by browser and Android battery settings; this package does not claim guaranteed background adhan playback.
- Firebase is not configured; no private keys or project credentials were supplied.
- Android APK is built by GitHub Actions; it is not a signed Play Store production release.
- Please verify religious translations, names, and meanings with qualified sources before public release.

## Project structure
- `index.html` — current app shell and UI
- `manifest.json`, `sw.js` — PWA install/offline support
- `capacitor.config.json`, `package.json`, `scripts/` — Android packaging
- `.github/workflows/` — Pages deployment and Android build
- `README.md` — this guide

## Credits
- QuranEnc API: https://quranenc.com/bn/home/api/
- Asma ul Husna list: common traditional enumeration; see discussion at https://muttaqi.app/99-names-of-allah/
