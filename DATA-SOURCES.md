# Data sources and attribution

## Quran
The full-surah reader requests Arabic text and Bengali translation from the QuranEnc public API (`https://quranenc.com/api/v1`). The app discovers a Bengali translation and prefers the Dr. Abu Bakr Muhammad Zakaria translation where the API lists it. Attribution is shown in the Quran reader. Keep the API's translation attribution and usage conditions intact; the first load requires internet. Quran text is not bundled in this ZIP.

## Location
GPS is provided by the device/browser Geolocation API. Reverse geocoding, when available, uses OpenStreetMap Nominatim. Manual administrative-area labels are user-editable.

## Calendar
Gregorian date uses the device date. Bangla date is calculated using Bangladesh's revised fixed calendar rule. Hijri date uses the browser Intl Umm al-Qura calendar; it is not an official Bangladesh moon-sighting determination.

## Asma-ul-Husna
The app includes a commonly used educational enumeration of 99 names. Scholars and published lists differ in the enumeration of the specific 99-name list; the note in the app explains this. The names of Allah are not limited to 99.
