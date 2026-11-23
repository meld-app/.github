# Security Policy — MELD (`@meld-app`)

## Sandbox & Privacy Guarantees
- **100% On-Device Execution:** File conversions, PDF/PPTX rendering, OCR, audio transforms, and image processing execute locally without network transmission.
- **Zero Internet Permission:** `meld-android` omits `android.permission.INTERNET` from `AndroidManifest.xml`; `meld-mac` runs without cloud dependencies or Accessibility hooks.
- **Scoped File Sharing & Bounded Inputs:** Android sharing exposes only temporary cache `outputs/` via `FileProvider` with explicit read grants and enforces input size limits (`100 MB` import cap).
- **Permanent Redaction:** Redacting or sanitizing PDFs flattens affected pages to rasterized bitmaps so stripped text and XMP metadata cannot be recovered.

## Reporting a Vulnerability
Please report suspected security issues privately via **GitHub Security Advisories** in the affected repository:
- [`meld-android` Security Advisories](https://github.com/meld-app/meld-android/security/advisories/new)
- [`meld-mac` Security Advisories](https://github.com/meld-app/meld-mac/security/advisories/new)

Include:
1. Affected repository, version/tag, and platform OS version.
2. Clear reproduction steps or proof-of-concept file characteristics.
3. Expected vs. observed impact.

We acknowledge valid reports promptly and coordinate a patched, signed release before public disclosure.
