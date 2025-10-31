
# Floating Bubbles • Vibe Game Launcher

This is a lightweight, single‑file webpage you can host for free. It shows big floating bubbles with images. Clicking a bubble opens a **popup modal** with an **embedded game** (via `<iframe>`). There's also a **Back to portfolio** button.

---

## Files
- `index.html` – all HTML/CSS/JS (no frameworks)
- `assets/` – placeholder images (replace with your own 1:1 images)

---

## Quick Edit
Open `index.html` and change:
1. **Back link**
   ```js
   const PORTFOLIO_URL = "https://your-portfolio-url.example";
   ```
2. **Games + images**
   ```js
   const GAMES = [
     { label: "Hana Universe", href: "https://example.com/hana-game", img: "assets/hana.png" },
     ...
   ];
   ```
   - Replace `href` with your game URL (Itch.io, Vercel app, etc.).
   - Replace `img` with your image file (800×800px PNG/WEBP recommended).

> Note: Some sites block embedding in iframes (X-Frame-Options / CSP). If a game doesn't load in the popup, click **Open in new tab** (built in). If you control the game, allow embedding.

---

## Free Hosting Options

### Option A: **Vercel** (recommended)
1. Create an account: https://vercel.com
2. Click **New Project → Deploy**.
3. **Drag‑drop** this folder into Vercel (or push to GitHub and import).
4. Get your live URL like `https://bubbles-yourname.vercel.app`

### Option B: **Netlify**
1. https://app.netlify.com → **Add new site → Deploy manually**
2. Drag‑drop the folder → get a live URL like `https://bubbles-yourname.netlify.app`

### Option C: **Replit** (code in browser + host)
1. https://replit.com → New Repl → **HTML/CSS/JS**
2. Upload `index.html` and `assets/`
3. Click **Run** to get a live link

---

## Link from Webflow
In your Webflow Navbar, set **Playground** link to **External URL** and check **Open in New Tab**. Use your deployed URL, e.g. `https://bubbles-yourname.vercel.app`.

(Optional) If embedding back into a Webflow page via `<iframe>`, you can pass the back link dynamically:
```
https://bubbles-yourname.vercel.app/?back=https://your-portfolio.webflow.io/
```

---

## Accessibility & Mobile
- Keyboard: Enter/Space opens bubbles, **Esc** closes the popup.
- Reduced motion: respects `prefers-reduced-motion`.
- Responsive: bubble sizes scale on tablet/mobile.

---

## Customize
- Bubble sizes: in CSS variables `--bubble-size`, `--bubble-size-md`, `--bubble-size-sm`.
- Float vibe: in JS `SETTINGS` (duration, drift, delay, density).

Enjoy!
