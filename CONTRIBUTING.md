# Contributing to MELD

Thank you for helping make **MELD** faster, safer, and easier to use on Android and macOS.

---

## Core Requirements

Every contribution across `@meld-app` repositories must uphold:
1. **Offline & Zero-Cloud First:** Never introduce `INTERNET` permissions, external API calls, cloud fallbacks, analytics, or crash trackers.
2. **Scoped & Memory-Safe I/O:** Bound decoded bitmaps/ZIP entries cleanly and write temporary outputs only to scoped cache paths.
3. **Localized & Accessible UI (Android):** Place user-facing strings in `strings.xml`, preserve EN/ES parity tests, and respect large font scaling (`200%`) and light/dark themes.

---

## Pull Request Workflow

1. Fork or branch off `main` using a descriptive branch name (`feat/...`, `fix/...`, `docs/...`, `chore/...`).
2. Keep commits focused using Conventional Commits style (`feat:`, `fix:`, `docs:`, `chore:`, `test:`).
3. Verify locally before opening a PR:
   - **`meld-android`:**
     ```bash
     ./gradlew lintDebug lintRelease testDebugUnitTest testReleaseUnitTest assembleDebug --offline --console=plain
     ```
   - **`meld-mac`:**
     ```bash
     make app
     ```
4. Ensure all `.github/PULL_REQUEST_TEMPLATE.md` checklist items and automated CI checks pass cleanly.

---

## Governance & Review Authority

All pull requests targeting `main` are subject to MELD's [`GOVERNANCE.md`](https://github.com/meld-app/.github/blob/main/GOVERNANCE.md) and reviewed by code owner `@omrajput14`.
