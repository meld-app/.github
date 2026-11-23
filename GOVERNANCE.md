# MELD Organization Governance & Authority

This document establishes the decision-making model, repository rules, and release authority for all projects maintained under the **MELD (`@meld-app`)** GitHub organization.

---

## 1. Leadership & Authority

| Role | GitHub Handle | Authority & Responsibilities |
| :--- | :--- | :--- |
| **Founder, Lead Architect & Release Authority** | [`@omrajput14`](https://github.com/omrajput14) | Final architectural sign-off, organization administration, repository rulesets, `CODEOWNERS` review approval, release tag creation (`v*`), and production signing key stewardship. |

### Authority Boundaries
- **Maintainer Sign-Off:** Every change to protected default branches (`main`) requires adherence to organization quality gates and `CODEOWNERS` accountability (`* @omrajput14`).
- **Admin Bypass:** Repository Administrators and Organization Admins retain explicit ruleset bypass authority solely for emergency hotfixes, release operations, and verified automated maintenance.

---

## 2. Repository Branch & PR Rulesets

All flagship public repositories (`meld-android`, `meld-mac`, `.github`) enforce active rulesets targeting `main`:

1. **No Direct Deletion or Force Push:** Branch deletions and non-fast-forward history rewrites are blocked.
2. **Pull Request Workflow:** External contributions and routine feature work enter `main` through pull requests.
3. **Code Owner Review & Thread Resolution:**
   - Pull requests require approving review from `@omrajput14` (as designated in `CODEOWNERS`), dismiss stale approvals on new pushes, and require all review conversations to be resolved before merge.
4. **Mandatory CI Status Checks:**
   - **`meld-android`:** `build-android-apk` (`lintDebug`, JVM debug & release unit tests, debug & release APK assembly).
   - **`.github`:** `validate-governance` (community health docs, `CODEOWNERS`, and issue-form YAML schema verification).

---

## 3. Release & Signing Authority

- **Tag-Version Alignment:** Release tags (`vX.Y.Z` or `vX.Y.Z-beta.N`) must match the project build manifest (`app/build.gradle.kts` `versionName` on Android). Tag workflows abort automatically on mismatch.
- **Cryptographic Signing:** Production artifacts are built in GitHub Actions from tagged commits and signed with repository-managed credentials (`ANDROID_KEYSTORE_*` secrets on `meld-android`, producing verified `MELD-v*-Android.apk` + `.apk.sha256` bundles).
- **Private Key Custody:** Signing keys and passwords are never committed to source control (`*.jks` and `*.keystore` are excluded via `.gitignore`).

---

## 4. Non-Negotiable Architecture Invariants

No pull request may weaken MELD's privacy guarantees:
1. **Zero Network Permissions / Cloud Calls** in application binaries (`android.permission.INTERNET` is forbidden in `meld-android`).
2. **Zero Telemetry or Tracking SDKs.**
3. **Irreversible Redaction & Metadata Sanitization** where promised in UI.
