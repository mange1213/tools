# Tool App repair package

This ZIP contains the site files at the ZIP root, ready to upload to the root of the GitHub Pages repository (the same folder as `index.html`).

## Changes made
- Restored missing equipment checkout and check-in handlers.
- Fixed touch selection so tapping a row/checkbox/label does not toggle the checkbox twice.
- Added equipment and worker add/edit forms and the missing archive/history actions referenced by the interface.
- Added checkout/check-in history events and dashboard/list refresh after successful saves.
- Removed photo upload controls from the restored equipment form. Existing stored photo data is not deliberately deleted.
- Corrected archived equipment filtering and the duplicate semicolon in the service-worker cache declaration.
- Kept the manifest and icons at the site root with relative paths suitable for GitHub Pages.

## Before uploading — important
1. Open your CURRENT live app and go to **Backup & Restore**.
2. Tap **Download Backup** and make sure the JSON backup file is saved somewhere you can find it.
3. In GitHub, download a ZIP of the current repository as a separate backup.
4. Extract this ZIP. Upload the files inside it (not the enclosing ZIP folder) to the repository root, replacing `index.html`, `sw.js`, and the other matching files when GitHub asks.
5. Commit the changes and wait for GitHub Pages to publish.
6. Check `https://YOUR-SITE/manifest.webmanifest` and `https://YOUR-SITE/icon-192.png`. Replace `YOUR-SITE` with your actual published site address.
7. Test checkout and check-in using one test item and worker before normal use. Confirm the counts and history update.

## Important limitations
This package passed JavaScript syntax checks, manifest JSON validation, ZIP integrity checks, and a static check that the inline buttons point to defined functions. It has **not** been tested on your live GitHub Pages deployment or with your live browser data. The app stores records in browser local storage, so use the backup first and do not clear site data. This ZIP cannot recover data already lost from a browser.
