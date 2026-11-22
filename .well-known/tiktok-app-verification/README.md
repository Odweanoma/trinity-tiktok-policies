# TikTok URL Ownership Verification — Readiness File

## Verification URLs (Production app)

The following URLs must be verified in the TikTok Developer Portal:

| URL | Purpose |
|-----|---------|
| https://odweanoma.github.io/trinity-tiktok-policies/ | Web/Desktop app URL |
| https://odweanoma.github.io/trinity-tiktok-policies/privacy.html | Privacy Policy URL |
| https://odweanoma.github.io/trinity-tiktok-policies/terms.html | Terms of Service URL |
| https://odweanoma.github.io/trinity-tiktok-policies/callback.html | OAuth Redirect URI |

## Verification Procedure

When you access the TikTok Developer Portal (Production mode → URL properties):

1. Click "Verify properties" for your app in Production mode
2. Choose "Verify by URL prefix" and enter each URL above
3. TikTok will provide a signature file — download it
4. Upload the signature file to the corresponding URL path on this GitHub Pages site
5. Click "Verify" to confirm ownership

## Signature File Placement

Place TikTok's provided signature file at the URL path TikTok specifies (typically under `/.well-known/` or a path indicated by TikTok during verification).

## Files in this Repository

- `callback.html` — OAuth callback page (receives authorization code + state)
- `index.html` — Gateway landing page
- `privacy.html` — Privacy Policy (discloses data collection, storage, and usage)
- `terms.html` — Terms of Service (governs app usage)
- `.well-known/tiktok-app-verification/` — Directory for TikTok signature files

## Notes

- No credentials, tokens, or secrets are stored in this repository
- The callback page runs entirely in the user's browser — no data is sent to GitHub or any third party
- Token exchange happens server-side in the private Hermes Debian environment
- This site is published via GitHub Pages at https://odweanoma.github.io/trinity-tiktok-policies/
