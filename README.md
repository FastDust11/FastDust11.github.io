# TrueNAS Backup — GitHub Pages OAuth information site

This is a static public information site for a **single-user, private, non-commercial** TrueNAS → Restic → Rclone → Google Drive backup workflow.

## Included files

- `index.html` — public application homepage
- `privacy.html` — privacy policy describing Google user data access and handling
- `terms.html` — short terms of use (optional but available in Google Branding)
- `style.css` — responsive styling; no scripts, trackers or external dependencies
- `.nojekyll` — publish files as static files without Jekyll processing

**No account credentials, tokens, TrueNAS addresses, OAuth client secrets, or personal files should be uploaded to this public repository.**

## Publish for free using GitHub Pages

1. In GitHub, create a **public** repository named exactly `<YOUR_GITHUB_USERNAME>.github.io`. Do not include angle brackets in the name.
2. Upload the files from this folder **directly into the repository's root** (not a nested `TrueNAS-Backup-GitHub-Pages` folder).
3. Open repository **Settings → Pages**.
4. Under **Build and deployment**, set **Source: Deploy from a branch**, then **main / (root)** and save.
5. Visit `https://<YOUR_GITHUB_USERNAME>.github.io/` and ensure that all three pages open without login. Publishing may take several minutes.
6. In Google Cloud → Google Auth Platform → **Branding**, enter:
   - **Application name:** `TrueNAS Backup`
   - **Application home page:** `https://<YOUR_GITHUB_USERNAME>.github.io/`
   - **Application privacy policy link:** `https://<YOUR_GITHUB_USERNAME>.github.io/privacy.html`
   - **Application terms of service link:** `https://<YOUR_GITHUB_USERNAME>.github.io/terms.html` (optional)
   - **Authorized domains:** `<YOUR_GITHUB_USERNAME>.github.io` if accepted by the Google Cloud form.
7. Keep the Google support/developer contact email set to an address you control, and save Branding.
8. In **Audience**, check whether Google enables **Publish app**. If Google requests domain ownership verification, follow its current requirements: GitHub Pages does not guarantee acceptance. Do not use an unrelated domain you cannot verify.

> Rclone's official Google Drive setup guide explicitly suggests a free GitHub Pages site for the personal-app publishing requirement. Google's formal verification guidance can still require proof that you control the domain. Both facts should be considered; this is not a guaranteed workaround.

## Accuracy checklist

Please use these files only if they accurately describe your setup:

- Backups are encrypted locally by Restic before upload.
- Rclone uses OAuth with the `drive.file` permission and only the owner's Google account.
- The repository password is not stored in the Google Drive repository.
- The application is personal, is not offered to third parties, and does not collect data for analytics/advertising.
- The privacy policy's description of retention, deletion and storage matches your actual configuration.

**This public site is informational only.** It does not handle OAuth redirects or store OAuth tokens. OAuth authorization will be performed by the Rclone desktop flow later, not through the GitHub Pages site.

## Sources

- Rclone Google Drive setup: https://rclone.org/drive/
- GitHub Pages quickstart: https://docs.github.com/en/pages/quickstart
- Google OAuth policy: https://developers.google.com/identity/protocols/oauth2/production-readiness/policy-compliance
