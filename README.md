# 漢讀 HanRead — Landing Page

Phase-0 waitlist landing page for HanRead: paid Substack subscriptions delivered to your Kindle/Kobo as a clean weekly EPUB digest, built for Traditional-Chinese readers.

## Files

- `index.html` — the entire site (single file, no build step, no framework)

## Setup required before going live

### 1. Formspree (waitlist form)

The email-capture form posts to Formspree. You need a free account and a form ID:

1. Go to <https://formspree.io> and sign up (free tier is plenty for a waitlist).
2. Click **+ New Form**, give it a name (e.g. "HanRead Waitlist"), and set the notification email to yours.
3. Copy your **Form ID** — it looks like `xyzabcde` (8 characters after `/f/` in the endpoint URL).
4. Open `index.html` and find this line (search for `REPLACE_WITH_FORM_ID`):
   ```html
   action="https://formspree.io/f/REPLACE_WITH_FORM_ID"
   ```
   Replace `REPLACE_WITH_FORM_ID` with your actual form ID, e.g.:
   ```html
   action="https://formspree.io/f/xyzabcde"
   ```
5. Commit and push.

### 2. GitHub Pages

1. Go to your repo on GitHub → **Settings** → **Pages**.
2. Under **Source**, choose **Deploy from a branch**.
3. Select branch `main`, folder `/ (root)`, and click **Save**.
4. After a minute or two, the site will be live at `https://kevinliu217.github.io/hanread/` (or your custom domain if you add one).

## Local preview

No build step needed — just open `index.html` in a browser:

```bash
open index.html
```

Or serve it with any static file server:

```bash
npx serve .
```
