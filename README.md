# maxthomason.github.io

Public site for the Business_Apps venture (this folder is its own git repo, gitignored by the main workspace repo):

- `/` — portfolio / credibility page linked from outreach emails.
- `/apps/<client-slug>/privacy.html` and `terms.html` — hosted legal pages for client apps (Apple requires a live privacy-policy URL). app-store-ship generates the content; convert to HTML here, push, and the URL goes into App Store Connect.

Deploy = `git push` (GitHub Pages serves `main` automatically).
