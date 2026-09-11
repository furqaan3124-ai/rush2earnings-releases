# Rush2Earnings — Android releases

Download host for the Rush2Earnings Android app. This repo holds the built APK
only; the source lives in the main `rush2earnings` repository.

## Download

**[rush2earnings.apk](https://github.com/furqaan3124-ai/rush2earnings-releases/raw/main/rush2earnings.apk)** — Android 7.0+, arm64

The website's "Download APK" buttons (Overview page and the foot of the sidebar)
point at that URL via `APK_URL` in `App.tsx`.

## Installing

Android blocks APKs from outside the Play Store by default. On first install the
phone will ask you to allow installs from your browser — that prompt is expected.

## Notes

- **This repo must stay public** for the download links to work. A private repo
  returns 404 to logged-out visitors, so the buttons would silently fail.
- Built arm64-only, which covers every phone sold since roughly 2015 and keeps
  the download at ~34 MB instead of ~84 MB.
- Signed with the release keystore in the main repo's `mobile/credentials/`.
  That signature must stay the same forever: Android refuses to upgrade an
  installed app if the key changes, and users would have to uninstall first —
  losing their session. It is also the SHA-1 registered with the Google
  Sign-In OAuth client, so re-signing breaks Google login too.

## Updating

Replace `rush2earnings.apk` and push. The download URL never changes, so the
website needs no redeploy.
