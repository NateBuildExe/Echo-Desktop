# Echo Desktop — Test and Issue Log

User-reported outcomes are labelled as such; they are not represented as independently reproduced tests.

## 1.10.0 — Windows installer acceptance

- **Date:** 15 November 2026
- **Tester:** Project owner
- **Environment:** Windows; exact edition/build and hardware not recorded
- **Installer:** `Echo-Desktop-Setup-1.10.0-x64.exe`
- **Test type:** Owner-reported manual acceptance
- **Overall:** **PASS — owner-reported**

| Check | Result | Recorded outcome |
|---|---|---|
| Build installer on Windows | PASS | Owner confirmed installer was built |
| Run Setup.exe | PASS | Owner confirmed installer runs |
| Complete installation | PASS | Owner reported installation working |
| Launch Echo | PASS | Owner reported app working |
| Start Menu shortcut | PASS | Included in owner's all-good confirmation |
| Desktop shortcut | PASS | Included in owner's all-good confirmation |
| Existing music library preserved | PASS | Owner explicitly confirmed library preserved |
| Uninstall behaviour | PASS | Owner confirmed uninstall worked |
| Library retained after uninstall | PASS | Owner explicitly confirmed library was not deleted |

**Evidence:** Owner captured UI screenshots but has not supplied them to this documentation update. Add them under `docs/screenshots/` when available.

**Record limitations:** Exact Windows build, hardware, installer hash and screenshots are not recorded. The assistant did not independently execute the installer.

## Reusable entry template

### VERSION — test title
- Date:
- Tester:
- Environment:
- Build / installer:
- Test type: Automated / Manual / Owner-reported
- Overall: PASS / FAIL / BLOCKED / PARTIAL

| Test | Result | Notes / evidence |
|---|---|---|
| | | |

**Problems found:**  
**Fixes applied:**  
**Retest:**  
**Remaining issues / limitations:**
