# Echo Desktop — Test and Issue Log

User-reported outcomes are labelled as such; they are not represented as independently reproduced tests.

## 1.10.0 — Windows installer acceptance

- **Date:** 15 November 2026
- **Tester:** Nate
- **Environment:** Windows; exact edition/build and hardware not recorded
- **Installer:** `Echo-Desktop-Setup-1.10.0-x64.exe`
- **Test type:** manual acceptance
- **Overall:** **PASS**

| Check | Result | Recorded outcome |
|---|---|---|
| Build installer on Windows | PASS | installer was built |
| Run Setup.exe | PASS | installer runs |
| Complete installation | PASS | installation working |
| Launch Echo | PASS | app working |
| Start Menu shortcut | PASS | Included in owner's all-good confirmation |
| Desktop shortcut | PASS | Included in owner's all-good confirmation |
| Existing music library preserved | PASS | explicitly confirmed library preserved |
| Uninstall behaviour | PASS | Owner confirmed uninstall worked |
| Library retained after uninstall | PASS | explicitly confirmed library was not deleted |

**Evidence:** captured UI screenshots and has been supplied them to this documentation. visit `docs/screenshots/`

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
