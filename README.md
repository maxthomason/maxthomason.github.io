# maxthomason.github.io

Public site for the Business_Apps venture (this folder is its own git repo, gitignored by the main workspace repo):

- `/` — portfolio / credibility page linked from outreach emails.
- `/apps/<client-slug>/` — one microsite per client app, stamped from `/apps/_template/`:
  - `index.html` — brand landing: app icon, tagline, App Store badge, support contact. This one URL serves as **support URL and marketing URL** in App Store Connect.
  - `privacy.html` — hosted privacy policy (Apple requires a live URL). Content converted from `clients/<slug>/store/privacy-policy.md`.
  - `terms.html` — hosted terms of use, converted from `clients/<slug>/store/terms-of-use.md`.
  - `icon.png` — the app icon (the 1024 master scaled down is fine).

To stamp a client microsite (app-store-ship does this): copy `_template/` → `<slug>/`, fill every `⟪…⟫` placeholder (brand accent hex comes from `design-tokens.json`), drop in `icon.png`, replace the `⟪CONTENT⟫` comment blocks in privacy/terms with the HTML conversion of the store docs. No `⟪…⟫` may remain — grep before pushing.

Deploy = `git push` (GitHub Pages serves `main` automatically). The privacy URL must be live **before** App Store submission.
