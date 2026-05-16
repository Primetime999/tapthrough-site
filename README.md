# tapthrough-site

The marketing + legal site for TapThrough. Three static HTML pages, one CSS file, no build step.

Lives at **https://tapthrough.app**.

## Pages

| URL | File | Purpose |
|---|---|---|
| `/` | `index.html` | Landing — name, pitch, support email, App Store badge (when live) |
| `/privacy` | `privacy.html` | Apple-required Privacy URL. Placeholder until iubenda activates. |
| `/terms` | `terms.html` | Required by App Store guideline 3.1.2(a) for auto-renewing subs. Linked from in-app paywall. |

URL constants are wired in the iOS app at `TapThrough/Services/LegalURLs.swift`. **Do not change the paths** without updating that file.

## Local preview

Any static server works. Easiest:

```bash
cd tapthrough-site
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy — first time setup (~15 min)

### 1. Push this directory to its own GitHub repo

```bash
cd tapthrough-site
git init
git add .
git commit -m "initial site scaffold"
gh repo create Primetime999/tapthrough-site --public --source=. --push
```

A separate public repo is recommended over keeping the site inside the private `Primetime999/Apps` repo — Cloudflare Pages reads from the repo, and you don't want to grant it access to the iOS source.

### 2. Connect Cloudflare Pages to the repo

1. https://dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Select `Primetime999/tapthrough-site`.
3. Build settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `/`
4. Click **Save and Deploy**. First build takes ~30 seconds.

The site is now live at `https://tapthrough-site.pages.dev`.

### 3. Attach the custom domain

1. In the Pages project → **Custom domains** → **Set up a custom domain**.
2. Enter `tapthrough.app`. Cloudflare auto-configures DNS because the domain is already at Cloudflare.
3. Repeat for `www.tapthrough.app` (or set up a redirect rule from `www` → apex).
4. Wait ~1 minute for SSL provisioning. Verify https://tapthrough.app/ loads.

### 4. Set up support email forwarding

1. https://dash.cloudflare.com → select `tapthrough.app` → **Email** → **Email Routing** → **Get started**.
2. Cloudflare adds the required MX records automatically.
3. Add a destination address (your real inbox) and verify via the email Cloudflare sends.
4. Create a custom address: `support@tapthrough.app` → forward to your verified destination.
5. Test: send mail to `support@tapthrough.app` from another account; confirm it arrives.

Apple reviewers do email this address — make sure it works before submitting.

### 5. Verify before App Store submission

```bash
for url in https://tapthrough.app/ https://tapthrough.app/privacy https://tapthrough.app/terms; do
  echo "$url"; curl -sI "$url" | head -1
done
```

All three should return `HTTP/2 200`.

## Updating content

Edit the HTML files, commit, push. Cloudflare Pages auto-deploys on every push to the default branch.

## Future: iubenda swap

When the iubenda subscription activates and generates real Privacy + Terms documents:

- Option A (preferred): replace the body of `privacy.html` and `terms.html` with the iubenda-generated content. URLs stay stable; iOS app needs no rebuild.
- Option B: 301-redirect `/privacy` and `/terms` to the iubenda-hosted URLs via Cloudflare Pages `_redirects` file. Slightly worse UX (extra hop) but keeps the legal copy in iubenda's editor.

The `LegalURLs.swift` doc comment commits to keeping these constant paths stable across that swap. Do not break that contract.
