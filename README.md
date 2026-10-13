# NHL Live — PWA starter

Mobile-first installable web app with live scores, team favorites, schedule, and standings.

## Data provider
This starter uses the public NHL web endpoints:
- `https://api-web.nhle.com/v1/score/now`
- `https://api-web.nhle.com/v1/schedule/YYYY-MM-DD`
- `https://api-web.nhle.com/v1/standings/now`

These are public NHL web endpoints rather than a guaranteed, documented commercial API. NHL may change them or restrict access; for a production app, verify the NHL's terms and consider a supported licensed provider (for example, SportsDataIO) if you need a contractual uptime guarantee.

## Run locally
Because service workers require localhost or HTTPS, serve the folder rather than opening `index.html` directly.

Python:
```bash
python -m http.server 8080
```
Then open `http://localhost:8080`.

## Install on Android
1. Host the folder on an HTTPS static host (GitHub Pages, Netlify, or similar).
2. Open the URL in Chrome on Android.
3. Use Chrome menu → **Install app** or **Add to Home screen**.

## Notes
- Score refresh: every 15 seconds while the page is visible.
- Favorites are stored locally on the device/browser.
- Notifications are intentionally not included.
- No backend or API key is required for this prototype.
- If the data endpoint changes, update `API` and response parsing in `index.html`.
