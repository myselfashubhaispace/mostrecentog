# OG Hub™ — Results-Driven Influencer Marketing Agency

Official landing page and website codebase for **OG Hub™** (<https://www.oghub.in/>), founded by **Ashutosh Mishra**.

Built with a high-conversion, neo-brutalist aesthetic, high-performance responsive layout, client-side validation, and instant email lead capture.

---

## ⚡ Quick Start (Local Server)

Run the zero-dependency local development server:

```bash
# Using Node directly (no install required)
node server.js

# Or using npm
npm start
```

Open your browser and navigate to:
**`http://localhost:3000`**

---

## 📬 Form Submissions & Email Setup

All strategy call requests and lead applications submitted on the form are routed directly to:
👉 **`oghub.in@gmail.com`**

### How it works:
1. **FormSubmit Integration:** The form action is configured with `https://formsubmit.co/oghub.in@gmail.com`.
2. **Instant AJAX Submission:** The client-side JavaScript attempts asynchronous submission for a fast user experience, then redirects to `thank-you.html`.
3. **Fail-safe Fallback:** If JavaScript or fetch is blocked (e.g. by strict ad-blockers), the form falls back to native HTML POST so no lead is ever lost.
4. **First Submission Note:** On the very first form submission, FormSubmit will send a 1-click confirmation email to `oghub.in@gmail.com` to activate email forwarding. Simply click "Activate Form" in that email once.
5. **Netlify Forms Ready:** When hosted on Netlify, the form also includes `data-netlify="true"` for automatic tracking inside your Netlify dashboard.

---

## 📊 Analytics & Tracking Scripts

Placeholders are pre-configured in the `<head>` of [`index.html`](file:///z:/adskunal/index.html):

| Platform | Variable / Location in `index.html` |
| :--- | :--- |
| **Meta Pixel** | `window.META_PIXEL_ID = 'YOUR_PIXEL_ID'` (Line ~43) |
| **Google Analytics 4** | `window.GA_MEASUREMENT_ID = 'G-XXXXXXXXXX'` (Line ~60) |
| **Microsoft Clarity** | `window.CLARITY_ID = 'YOUR_CLARITY_ID'` (Line ~76) |

*Note: Safe stubs are provided so there will be zero JavaScript console errors if these IDs are not yet set.*

---

## 🚀 Deployment Options

### 1. Netlify (Recommended)
- Push this folder to a GitHub repository or drag-and-drop the folder into [Netlify Drop](https://app.netlify.com/drop).
- `netlify.toml` is already included and configured.

### 2. Vercel
- Import this repository on [Vercel](https://vercel.com).
- `vercel.json` is already included with clean URLs enabled.

### 3. GitHub Pages
- Go to repository Settings > Pages > Select `main` branch root `/` > Save.

---

## 📂 Project Structure

```text
├── index.html         # Main landing page for OG Hub (Ashutosh Mishra)
├── thank-you.html     # Branded conversion thank-you page
├── privacy.html       # Privacy policy updated for OG Hub
├── server.js          # Zero-dependency local Node.js development server
├── package.json       # Project configuration and start scripts
├── netlify.toml       # Netlify configuration & redirects
├── vercel.json        # Vercel configuration & clean URLs
├── assets/
│   ├── oghub-logo.png             # Official OG Hub logo
│   ├── ashutosh.jpg               # Ashutosh Mishra portrait & banner
│   ├── ashutosh-portrait.jpg      # Founder avatar
│   ├── logos-trimmed/             # Partner & brand logos (Himalaya, OLX, Tata MF, etc.)
│   └── proofs/                    # Real campaign screenshots, analytics & portal views
└── README.md          # Documentation & setup guide
```

