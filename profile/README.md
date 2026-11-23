<p align="center">
  <img src="https://raw.githubusercontent.com/meld-app/.github/main/assets/MELDLogo.png" alt="MELD Logo" width="144" />
</p>

<h1 align="center">MELD</h1>
<p align="center"><strong>TRANSFORM • CONVERT • ORGANIZE — 100% Local &amp; Offline</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/Cloud_Uploads-Zero-1F8A5B?style=for-the-badge" alt="Zero Cloud" />
  <img src="https://img.shields.io/badge/Telemetry-None-1F8A5B?style=for-the-badge" alt="Zero Telemetry" />
  <img src="https://img.shields.io/badge/Platforms-macOS_%26_Android-FF6B4A?style=for-the-badge" alt="macOS and Android" />
  <img src="https://img.shields.io/badge/Releases-Cryptographically_Signed-2E64E5?style=for-the-badge" alt="Signed Releases" />
</p>

---

## About MELD

**MELD** builds native, zero-cloud file transformation studios for **Android** and **macOS**. Every conversion, compression, redaction, background removal, slide render, and archive workflow runs strictly on-device — no servers, no uploads, no accounts, and no telemetry.

---

## Flagship Repositories

| Repository | Platform & Release | Stack & Highlights | Download |
| :--- | :--- | :--- | :--- |
| [**`meld-android`**](https://github.com/meld-app/meld-android) | **Android (`v2.1.0`)** | Kotlin 2.0 + Jetpack Compose (Material 3), Android SDK 26–35, **40 local engines** across PDF, PPTX Slides, Images, Audio, Tables & Archives, Customizable Home, Light/Dark & EN/ES UI | [Signed APK (`v2.1.0`)](https://github.com/meld-app/meld-android/releases/tag/v2.1.0) |
| [**`meld-mac`**](https://github.com/meld-app/meld-mac) | **macOS (`v2.1.0-beta.1`)** | Swift 6 + AppKit, SwiftUI, PDFKit, Vision, ImageIO & AVFoundation; Zero-Click Radial Wheel (`⇧ Shift` Convert, `⌘ Command` Tools, `⌃ Control` Actions), Float Shelf & FlipDoc Studio | [Signed `.dmg` (`v2.1.0-beta.1`)](https://github.com/meld-app/meld-mac/releases/tag/v2.1.0-beta.1) |

---

## Cross-Platform Studio Capabilities

| Domain | `meld-android` | `meld-mac` |
| :--- | :--- | :--- |
| **PDF Studio** | PNG/JPG (`.zip` or `1..N`), Markdown, HTML5 reader, `.docx`, `.txt`, Compress, 2/3/4-up Handout, visual Split, Stamp, flatten Redact, Merge queue, Sanitize | `.xlsx`, `.docx`, `.rtf`, `.html`, `.md`, `.txt`, PNG/JPG, Compress, 3-up Handout, Lock & Stamp (+ AES Password), PII Redact, Page Organizer, Split, Merge, Vision OCR |
| **PPTX & Slides** | Pure-Kotlin OOXML parser & vector PDF, multi-slide/single-slide PNG/JPG, Markdown, HTML5 reader, `.docx`, `.txt`, Slide Handout, losslessly Sanitize PPTX | Cross-platform slide & document workflows |
| **Image Studio** | JPG/PNG/WebP/BMP/TIFF, 1–12 photo Image-to-PDF, BFS flood-fill Remove BG, Compress to KB, Resize & Frame, 1–9 Photo Collage, Strip EXIF, QR Studio | JPG/PNG/WebP/HEIC/AVIF/TIFF/PDF, 1-click Remove BG, Size-limit Compress, Scan/Generate QR, PII Redact, Resize & Frame, Photo Collage, Vision OCR, Strip EXIF |
| **Spreadsheets & Docs** | CSV/TSV to paginated vector PDF, Markdown tables & structured JSON | XLSX/CSV/TSV/DOCX/RTF/MD/HTML cross-conversions |
| **Audio, Video & Subtitles** | Audio Waveform PNG, Speed 2x offline WAV | Video to MP4/MOV/GIF/M4A/WAV, Mute Audio, PNG Snapshots, Audio format/Mono conversions, SRT/VTT/TXT subtitles |
| **Archives** | Deduplicated multi-file `.zip` Archive | `.zip`, `.tar.gz`, `.tar` & sibling-folder Extraction |

---

## Security, Signing & Zero-Cloud Guarantee

- **Zero Network Footprint:** `meld-android` declares no `android.permission.INTERNET`, and all temporary outputs stay in scoped cache paths (`FileProvider` `outputs/` scope).
- **Destructive Privacy Operations:** PDF Redaction and Sanitization flatten pages so hidden text layers and metadata are permanently stripped.
- **Cryptographic Release Verification:** Signed release artifacts publish with accompanying `.sha256` digests (`RSA-4096` APK signing on `meld-android`, signed `.dmg` releases on `meld-mac`).

---

## Governance, Rules & Authority

All repositories under `@meld-app` follow standardized governance, automated CI verification, protected `main` branch rulesets, and explicit code-owner authority:

- [**Governance & Authority (`GOVERNANCE.md`)**](https://github.com/meld-app/.github/blob/main/GOVERNANCE.md) — Leadership (`@omrajput14`), maintainer authority, protected-branch rulesets, and release signing rules.
- [**Security Policy (`SECURITY.md`)**](https://github.com/meld-app/.github/blob/main/SECURITY.md) — Zero-cloud sandbox guarantees and coordinated vulnerability reporting.
- [**Contributing Guide (`CONTRIBUTING.md`)**](https://github.com/meld-app/.github/blob/main/CONTRIBUTING.md) — Local test/lint checklists and pull request workflow.
- [**Code of Conduct (`CODE_OF_CONDUCT.md`)**](https://github.com/meld-app/.github/blob/main/CODE_OF_CONDUCT.md) — Community standards across issues, PRs, and discussions.
- [**Support (`SUPPORT.md`)**](https://github.com/meld-app/.github/blob/main/SUPPORT.md) — Checksum verification and issue reporting channels.
