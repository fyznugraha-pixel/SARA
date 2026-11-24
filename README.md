# SARA - SAP Automated Root-Cause Analyzer (Education Edition)

Official binary distribution & release channel for **SARA (SAP Automated Root-Cause Analyzer)**.

- **Developer:** Fayiz Apriwansyah Nugraha
- **Affiliation:** Telkom University
- **License:** Internal / Education (Closed Source - All Rights Reserved)
- **Latest Version:** `v1.1.1`

## Download & Installation

1. Open the **Releases** section of this repository.
2. Download **`SARA_Setup.exe`** from the latest release (`v1.1.1`).
3. Run `SARA_Setup.exe` on Windows 10/11 64-bit (installs per-user without Admin/UAC and without requiring Python).
4. Optional: verify file integrity against [`SHA256SUMS.txt`](SHA256SUMS.txt).

## Prerequisites for Live SAP Features

To connect SARA to live SAP GUI (Module Audit, Class Batch, Live Diagnosis, Doc Flow, X-Ray, Health Check), both sides must allow SAP GUI Scripting:

1. **SAP Server (Mandatory - Basis / Admin):** parameter `sapgui/user_scripting = TRUE` in `RZ11`.
2. **SAP Logon Client (Windows):** `Options -> Accessibility & Scripting -> Scripting -> Enable scripting` checked, with both notification checkboxes unchecked.

Offline features (Demo Mode, SAP Glossary, Error KB, PDF/AI Module Extraction) work without SAP GUI Scripting.
