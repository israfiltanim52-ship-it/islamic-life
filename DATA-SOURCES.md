# Data Sources and Verification

- Quran text/translation loading in the existing app uses QuranEnc API (`https://quranenc.com/api/v1`). The app caches visited surahs locally. Confirm translation key, source attribution and API terms before public release.
- 15-line Hifz Quran layout reference requested by the project: `https://amalkit.com/15-line-quran`. The licensed source pages/data for the exact Imdadia Noorani edition were not included in the supplied ZIP, so this build does not fabricate or claim exact page/line matching.
- Prayer-time calculations are implemented locally in the existing app and are approximate. Users should compare with their local mosque timetable.
- Madrasa directory data was not supplied. No unverified institution records have been invented.
- Firebase project credentials, Authentication, Firestore, Storage and Security Rules were not supplied or connected.
