# Comeback OS V8.1 — Reliability release (Phase 2, step 1)

No new screens. This release makes V8 safer. Your data and the database (`comeback` / `kv`) are untouched.

## Changes
- A damaged record no longer crashes a screen. It shows "Unreadable record" with a Delete button.
- If a screen fails to render, a message appears with Go Home / Settings buttons. A startup error also shows a message instead of a blank page.
- Data format version added (`meta` key, schema 9). A one-time migration gives every record an id (needed to edit/delete). A full copy is saved first under `premigration-backup`.
- Backups now record `v:2` and `schema:9`. Older V6/V8 backups (v:1) still import; missing career collections default to empty.
- Import checks every record, and refuses the whole file (changing nothing) if any record is unreadable.
- Import and snapshot-restore now save a copy of your current data first (shown in Settings > Safety net).
- Validation: percentages and skill levels must be 0-100; URL fields must start with http:// or https://; a deadline cannot be before its start date.
- All Modules page now lists every module, including Career, Projects, Skills, Applications, Interviews, Certificates and Search.

## Tested (headless Chromium, 390px and 1280px)
Old-version data opens in V8.1 with all records kept; legacy records get ids; migration and backup written; 24 screens render; damaged grade, flashcard and revision records handled; invalid values rejected and valid ones saved; export format; corrupt import refused with data intact; good import with pre-import copy; old-format backup import; offline reload via service worker.

## Not tested
Real Android device, PWA install prompt, notifications, sound, screen reader.

## Deploy
1. Settings > Export JSON backup in the live app.
2. Upload every file in this folder to the repo root, replacing the old ones.
3. Open the site, reload twice. Settings should say version 8.1.

## Roll back
Re-upload the V8 files (Comeback-OS-V8-Phase1.zip). Data stays, since V8.1 only adds keys (`meta`, `premigration-backup`). If anything looks wrong, restore your exported backup in Settings.
