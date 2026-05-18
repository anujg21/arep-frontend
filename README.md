# AREP — Landing Page

Marketing site for [AREP](https://github.com/anujg21/arep), the runtime control plane for AI agents.

**Live:** deploy to Vercel in one command (see below).

---

## Stack

Single `index.html` — no build step, no framework, no dependencies to maintain.

- **Styling:** Tailwind via CDN + custom CSS
- **Fonts:** Inter + JetBrains Mono via Google Fonts
- **Forms:** [Formspree](https://formspree.io) (free tier)
- **Demo booking:** [Calendly](https://calendly.com) link

---

## Local preview

```bash
open index.html
```

Or serve it with any static server:

```bash
npx serve .
# → http://localhost:3000
```

---

## Deploy to Vercel

```bash
npm i -g vercel
vercel --prod
```

Vercel auto-detects the static HTML and deploys with HTTPS and a global CDN. Connect your custom domain under **Project → Settings → Domains**.

---

## Wire up the form

1. Sign up at [formspree.io](https://formspree.io) → **New Form**
2. Copy your form ID (e.g. `xpwzabcd`)
3. In `index.html`, find:
   ```js
   const FORMSPREE_ID = 'YOUR_FORM_ID';
   ```
   Replace `YOUR_FORM_ID` with your actual ID.

Submissions arrive in your email instantly. Enable reCAPTCHA in the Formspree dashboard to block spam.

---

## Wire up demo booking

1. Create a 30-min event at [calendly.com](https://calendly.com)
2. Copy your link (e.g. `calendly.com/yourname/arep-demo`)
3. In `index.html`, find the `demo-link` anchor and update `href`:
   ```html
   <a href="https://calendly.com/yourname/arep-demo" ...>
   ```

---

## Update and redeploy

After editing `index.html`:

```bash
# From the root arep/ repo:
git add landing/
git commit -m "update landing page"
git push                                      # updates github.com/anujg21/arep
git subtree push --prefix landing frontend main  # updates this repo
```
