# Support & Release Verification

Need help using **MELD** on Android or macOS? Start here:

---

## 1. Download Verified Releases

Always install builds exclusively from official GitHub Releases:
- **Android APK:** [`meld-app/meld-android/releases`](https://github.com/meld-app/meld-android/releases)
- **macOS App (`.dmg`):** [`meld-app/meld-mac/releases`](https://github.com/meld-app/meld-mac/releases)

Verify Android APK integrity locally:
```bash
sha256sum -c MELD-v2.1.0-Android.apk.sha256
apksigner verify --print-certs MELD-v2.1.0-Android.apk
```
Expected signing certificate subject: `CN=MELD for Android, OU=Mobile Studio, O=MELD, C=US`  
(`SHA-256` digest: `26448b78d839b7e8259d952fa65302e4edd61d3530eb1a2735497bc5464c1585`).

---

## 2. Reporting Bugs & Requesting Features

- **Android bugs / feature requests:** [Open an Android issue](https://github.com/meld-app/meld-android/issues/new/choose)
- **macOS bugs / feature requests:** [Open a macOS issue](https://github.com/meld-app/meld-mac/issues/new/choose)
- **Security vulnerabilities:** Follow [`SECURITY.md`](https://github.com/meld-app/.github/blob/main/SECURITY.md) — never post sensitive exploits in public issues.
