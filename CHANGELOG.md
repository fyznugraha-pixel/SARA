# Changelog - SARA (SAP Automated Root-Cause Analyzer)

## v1.1.3 (2026-11-25)

- **Exercise Scope Filter (Module Audit):** Added `All` / `From` / `Only` Exercise filtering (`Semua` / `Mulai dari` / `Khusus`) under `Advanced Options` for Built-in Module 1, Module 2, and Custom JSON/PDF modules, skipping SAP T-Code queries outside the chosen Exercise while recalculating scores and WA summaries accurately.
- **Per-Task Manual Score Rubrics:** Configure custom point weights per step (weight `0` excludes steps from grading, Root-Cause chains, and Class Top Bottlenecks), choose `Proportional (0-100)` vs `Direct Sum`, adjust passing thresholds and `WARN` partial credit, and re-score live without re-querying SAP.
- **Class Batch Detail Modal, Canvas Heatmap & Resume:** Double-click any student row or heatmap row to inspect step-by-step details (`Prev/Next`, status filters, Copy WA, PDF Slip, Load to Audit Tab); pixel-aligned scrollable Canvas Heatmap with hover tooltips; smart multi-row Excel roster header detection; automatic transient SAP UI error retry; and `Resume Remaining` batch recovery on disconnect.
- **Module 2 AR Accuracy & Generalized Bottlenecks:** Tolerant `Street` address comparison (`Platz`/`Pl` abbreviations and punctuation without cross-student false positives) plus generalized Class Top Bottleneck labels (`CSTOMERXX`).
- **License Activation System:** Added Ed25519-signed License Key verification with 1-device lock, 24-hour offline grace, and live bilingual (`ID / EN`) activation & status dialog.

## v1.1.2 (2026-11-24)

- **Compact, Decluttered UI:** Consolidated header controls into the `Settings` dropdown (Theme, Language, Pin, Check SAP, SAP Session), folded `CoCd / Plant / FY`, Evidence Screenshot, and Demo Mode into collapsible `Advanced Options`, moved secondary actions into the `More` menu, and added outside-click auto-dismiss across all dropdown menus.
- **AI Module Extract & Direct Module Management:** Shortened AI Import footer actions (`Review & Next` / `Cancel`) for HiDPI screens, replaced `Paste Clipboard` with a vector icon + tooltip, and added a direct confirmation-protected Delete button for custom modules on the `Modules & PDF` tab.
- **Safer Auto-Fix Confirmation Dialog:** Separated `Error Fixes (WRONG)` (checked by default) from `Incomplete Steps (MISSING)` (unchecked by default with an explicit warning) so unfinished student steps are never advanced unintentionally, with live selection counts and disabled Run state at 0 selected.
- **Cross-Module Accuracy Hardening (`FI/CO`, `MM/SCM`, `SD`, `PP`, `HCM/HR`, `SE16N`):** Refused partial `SE16N` filter execution + added `SELFIELDS` PageDown scrolling, added `GuiTree` reader & 3-decimal `MMBE` stock quantity parsing without false positives, filtered classic ABAP list headers, detected `VKM1` & FI/CO/HR authorization errors, cleared stale `MB51` user filters, and fixed contextual `customer_id`/`vendor_id` mapping on AI JSON import.

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
