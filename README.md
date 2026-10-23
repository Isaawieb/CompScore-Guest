# CompScore guest score sheets

A browser-only Yahtzee score sheet for guests invited by a CompScore host. Guests do not need to install CompScore or create an account.

The host creates a game, selects a player, and shows their invitation QR. The guest opens that invitation, records scores, and chooses **Submit Scores** to display a results QR. The host scans and confirms the result in CompScore.

## Privacy and offline use

Scores are stored in the guest's browser. This page does not upload scores, use analytics, or contact external QR services. The invitation is carried in the URL fragment. Normal website hosting requests still reach GitHub Pages.

A connection is required for the initial page load. Wait for **Ready for offline scoring** before disconnecting. Keep the invitation link and avoid private browsing or clearing browser data until the host confirms the score import.

## Hosting

This directory is the entire static website. GitHub Pages should serve branch `main`, folder `/ (root)`. The `.nojekyll` file preserves the buildless files.

Guest-page address for CompScore:

https://isaawieb.github.io/CompScore-Guest/

An invitation from CompScore is needed to open a personal score sheet. Visiting the base address alone displays instructions to obtain one.

When updating the webpage, increase the cache version in `sw.js`. Existing guests may need to reopen online to receive an update.

## Included library

`vendor/qrcode.js`: qrcode-generator 1.4.4 by Kazuhiko Arase, MIT licensed. Its license is included. CompScore's page design and application code are separate from this third-party library.

This is an independently designed companion score sheet, not an official publisher product. Yahtzee is a Hasbro trademark.
