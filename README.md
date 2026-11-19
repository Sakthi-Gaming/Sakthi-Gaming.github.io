# Karpom Karpippom — Play Store release kit

## 1. Host the app (GitHub Pages, free)
1. Create a public repo named exactly `Sakthi-Gaming.github.io` (root site, needed for the `.well-known` file).
2. Upload everything in this folder (including the hidden `.well-known` folder and `.nojekyll`).
3. Settings → Pages → Branch: `main` / root → Save.
4. Open https://sakthi-gaming.github.io on your phone in Chrome. "Add to Home screen" should appear.

## 2. Build the Android app (no Android Studio needed)
1. Go to https://www.pwabuilder.com, paste https://sakthi-gaming.github.io, click Start.
2. Package for stores → Android → Options:
   - Package ID: `com.karpom.app`
   - App name: கற்போம் கற்பிப்போம்
   - Signing key: "Create new" → DOWNLOAD AND BACK UP the key file + passwords. Losing it = you can never update the app.
3. Download the zip. It contains the `.aab` (upload to Play) and `assetlinks.json`.
4. Copy the SHA-256 fingerprint from that `assetlinks.json` into `.well-known/assetlinks.json` here and push.
   (After Play App Signing is enabled, also add the fingerprint shown in Play Console → Setup → App signing.)
   This removes the browser address bar inside the app.

## 3. Google Play Console
1. https://play.google.com/console → developer account, one-time US$25 fee, ID verification.
2. Create app → Name, Default language: Tamil, App, Free.
3. Store listing: use files in `/store` (icon 512, feature graphic 1024x500, phone screenshots).
4. App content:
   - Privacy policy URL: https://sakthi-gaming.github.io/privacy.html (put your email in it first)
   - Target audience: choose age groups (e.g. 5 & under, 6–8) → Families Policy applies
   - Ads: No · Data safety: No data collected · Content rating questionnaire: Everyone
5. Testing: new personal accounts must run a closed test with at least 12 testers for 14 days before production access.
6. Upload the `.aab` to Production → Review (usually a few days, longer for kids apps).

## Before submitting
- Replace YOUR-EMAIL@example.com in privacy.html.
- Get a Tamil teacher to check pazhamozhi meanings and romanization.
- Test on 2–3 Android phones (Tamil voice installed and not installed).
