# Prototype 2 — validation report

Validation date: 2026-11-13

## Checks passed
- JavaScript syntax check passed for `index.html` application code and `sw.js` using Node.js 22.
- Manifest JSON parsed successfully; the referenced 192×192 and 512×512 PNG icons exist.
- Content/data checks passed: 26 English letters, 50 Bengali school-chart entries/signs, 26 English word lessons, and 4 bilingual sentence lessons.
- Every Bengali entry in the current starter list has an example entry.
- Simulated interaction checks passed for Beginner letter matching, star award, parent dashboard totals, Bengali matching, the combined glyph `ড়`, the “Ice cream” word puzzle, a Pro sentence puzzle, and localStorage progress writing.

## Not verified yet
- Actual rendering and touch/drag behavior on the user's Android phone.
- Offline behavior after installation in Android Chrome.
- Availability and quality of Bengali speech on the user's specific Android device.
- Native APK/AAB compilation, signing, installation, or Play Store submission.

The simulated interaction checks are code-level tests; they are not a substitute for testing on a physical Android device.
