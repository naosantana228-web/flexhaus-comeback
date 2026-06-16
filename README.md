# FlexHaus — "The Comeback" booking page

A single-file, static three.js comeback-booking page for the FlexHaus retention campaign.
No backend, no build step — it runs straight off GitHub Pages.

## Run locally
Just open `index.html`, or serve it:
```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages
1. Create a public repo (e.g. `flexhaus-comeback`).
2. Upload `index.html` (and this README) to the repo root.
3. Repo **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save**.
4. Wait ~1 minute; your live URL is `https://<username>.github.io/flexhaus-comeback/`.

## Before a real launch
- Wire the form to a free-tier provider (Formspree action or a `mailto:` fallback). It currently
  captures the booking object to the browser console for the demo.
- Re-confirm mobile performance and the reduced-motion / no-WebGL fallbacks on the live URL.

## Notes
- The only stat shown ("~2× more likely to quit") is computed from `flexhaus_bookings.csv` (1.97x).
- Accessibility: keyboard-reachable form, visible focus, real labels, consent not pre-ticked,
  canvas is `aria-hidden`, graceful fallback when WebGL is unavailable or reduced-motion is set.
