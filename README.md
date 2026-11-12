# ARAV'S Little School — Prototype 2

A bilingual Bengali/English early-learning PWA prototype.

## What's improved in Prototype 2
- The answer slots now show a faint outline of the exact expected letter or word. Children match the real glyph/word shape instead of placing pieces into empty boxes.
- Beginner letter rounds now have one correct letter tile and two distractors.
- Regular word rounds contain 26 English A–Z vocabulary items; Pro has four short bilingual sentence-ordering rounds.
- Beginner includes 26 English letters and the common 50-entry Bengali school-chart set: 11 vowels plus 39 entries in the consonant section. The final entries include the special forms/signs ৎ, ং, ঃ and ঁ; some examples contain the target inside the word, and the card explains that where relevant.
- Stars and per-mode completed-level counts are saved in this browser's localStorage.
- A simple parent progress view shows stars and progress by learning mode.
- Voice feedback speaks the English and Bengali parts separately when the device has suitable speech voices.
- Added 192px and 512px PNG app icons and bumped the offline cache to v2. See `TEST_REPORT.md` for code-level validation and items still needing a physical-phone test.

## Run on Android (phone only)
1. Extract this ZIP on the phone.
2. Upload the folder contents to a static HTTPS host such as Netlify or GitHub Pages. Do not upload only the ZIP as a page.
3. Open the HTTPS page in Chrome on Android.
4. Use Chrome's menu → Install app / Add to Home screen.
5. Open once online so the service worker caches the app, then test it in airplane mode.

The parent dashboard and learning progress are local to that browser/device. Clearing Chrome site data can erase saved progress. Speech depends on the Android device's installed Bengali and English voices.

## Known limitations
- This is a shape-guided matching puzzle, not a precision-cut jigsaw with interlocking tabs. The target slots use the browser's rendered glyph outline as a visual guide.
- Bengali letter examples and vocabulary are a starter set and should receive review by a Bengali early-learning teacher before public release.
- Emoji are temporary illustrations; a polished release should use consistent, licensed child-friendly artwork and recorded/native-quality audio.
- The parent view is not password-protected. Do not treat it as a secure parental-control system.
- No APK has been built, signed, device-tested, or published as part of this prototype.

## APK / Play Store path
This folder is a static PWA, not a native Android project. For a signed APK/AAB, package it using a trusted TWA/PWA packaging workflow or wrap it with Capacitor, then build and sign it in Android Studio or a suitable cloud build environment. Keep the signing key private and backed up. Before Play Store submission, verify current target API, app-content, child/families policy, data-safety, testing, and store-listing requirements from the official Play Console documentation.

## Next step to reach an APK
Publish the extracted folder at a public HTTPS address first. The web manifest must be reachable at `https://your-domain/manifest.json`. Then use a TWA packaging flow (for example, PWABuilder/Bubblewrap) and configure Digital Asset Links for the exact signing certificate. Keep the signing key private and make a secure backup before publishing. The Bubblewrap CLI route needs a Node.js/JDK/Android build environment; if you do not have a computer, use a reputable cloud/GUI packaging service and verify its output before installing it.

As of 2026-11-13, new Google Play apps and updates must target Android 16 / API 36 or higher. A new personal Play Console account created after 2023-11-13 must also complete a closed test with 12 opted-in testers continuously for 14 days before applying for production access. Because this is child-directed learning software, the final app must accurately complete the Target Audience, Data safety and content-rating declarations and comply with Google Play Families policies. A TWA package should deliver a real, useful learning app—not merely a blank website wrapper.
