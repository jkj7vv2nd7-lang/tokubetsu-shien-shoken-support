# QA Report v9.2.1

## Static checks
- APP_VERSION: 9.2.1
- HTML IDs: 275
- Duplicate IDs: 0
- JavaScript syntax: PASS (Node.js `--check`)
- Main script blocks: 1
- Buttons: 198
- `10分で使ってみる`: present
- `❓ ヘルプ`: present
- `先生の仕事を1本につなぐ`: present

## Functional scope
Existing major functions are retained, including saving/history, change review, growth sheet, interview preparation, record summary, next support, annual review, class observation, portfolio, Excel export, JSON backup/restore, print, demo data, diagnostics, abnormal tests, scenario tests, and release gate.

## Browser verification
Local automated browser E2E is not claimed because the development environment blocks Chromium navigation by administrator policy. Final verification should be performed on the Vercel Preview deployment in a normal browser before merging to `main`.

## Release gate
Do not merge v9.2.1 into production until Preview verification confirms:
1. Version 9.2.1 is displayed.
2. Help and 10-minute guide open/close correctly.
3. Four dashboard flow buttons navigate correctly.
4. Existing core functions respond.
5. F12 Console has no red errors during normal operation.
6. Backup/restore and Excel/print remain usable.
