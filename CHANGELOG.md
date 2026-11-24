# Changelog - SARA (SAP Automated Root-Cause Analyzer)

## v1.1.1 (2026-11-24)

- **Responsive Audit Stop Button:** Added Stop (`Hentikan`) button on the Module Audit tab and instant mid-student cancellation in Class Batch with automatic SAP Easy Access (`/n`) recovery.
- **Cross-Module Stability (MM/SCM, SD, PP, SE16N):** Handled SAP GUI Virtual Key `617` (`The virtual key is not enabled`) gracefully with Execute/Enter fallback, enabled automatic `All Orders` selection in `VA05`, added early T-Code authorization detection, improved `ME2L` & `COOIS` field filters, and added per-step error isolation for custom JSON modules.
- **Scrollable Visual Module Editor:** Added vertical scrollbar and mouse-wheel scrolling to Selected Check Details so Filter and Fix Hint fields stay accessible on HiDPI screens, and preserved extra JSON check fields (`plant`, `state`, `usage`, `execute_vkey`, etc.) on save.
- **UI & Privacy Polish:** Minimalist vector icon buttons with bilingual tooltips, cleaner thread-safe in-app Update dialog layout, and removal of repository links from application UI and Windows installer metadata.
- **Complete Bilingual & Prerequisite Docs:** Full `ID / EN` translation across all 7 tabs, Glossary, Error KB, Guide, and dialogs, plus clear SAP Server Scripting (`RZ11: sapgui/user_scripting = TRUE`) setup guidance.

## v1.1.0 (2026-11-24)

- Class Batch Audit, Student Roster Import (`.csv` / `.xlsx`), Class Progress Heatmap, Top Bottleneck Analytics, and Excel (`.xlsx`) / CSV gradebook export.
- Root-Cause Chain Analysis, Double-Posting Detector, Cross-Student Target Guard, and Weighted Rubric Scoring (0-100).
- SQLite Audit History & Progress Diff, Branded PDF Score Slips, and Automatic SAP Screen Evidence Capture Pack.
- Live Watch Mode (2s polling), Performance Assistant Summary, Document Flow Tracer (`VA03`/`FB03`/`ME23N`), SAP Screen X-Ray, Visual Rule Recorder, and 5-Point Pre-Flight Check.
- Offline SAP Glossary (46 entries), Editable Error KB Explorer, Read-Only Guardrail Policy Viewer, Interactive Guide tab (6 Playbooks + 47 Features), Command Palette (`Ctrl+K`), Co-Pilot Checklist, Multi-Session SAP Picker, Offline Demo Mode, Team Packs (`.sara-pack.json`), Support Diagnostic Zip, and In-App Auto-Updater.

## v1.0.0 (2026-11-16)

- Initial release of SARA (SAP Automated Root-Cause Analyzer) with built-in Module 1 (AP) & Module 2 (AR) audits, universal multi-module JSON support, automatic PDF extraction, Visual Module Editor, Active Screen Diagnosis, Universal Health Check, Dark/Light themes, and Windows installer (`SARA_Setup.exe`).
