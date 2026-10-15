# Community Food Finder

A static, GitHub Pages-ready food assistance locator using Leaflet and OpenStreetMap.

## Deploy
1. Create a public GitHub repository.
2. Upload `index.html` and `locations.json` to its root.
3. Open Settings > Pages > Build and deployment > Deploy from a branch.
4. Select `main` and `/ (root)` and save.
5. Open the published URL shown in GitHub Pages.

## Data
Replace all demo records in `locations.json` with verified programs before public launch. Each record requires a unique `id`, numeric `lat` and `lng`, and should include `name`, `type`, `address`, `town`, `zip`, `days` (array), `hours`, and `phone`.

## Notes
- The geocoder uses the public OpenStreetMap Nominatim endpoint, subject to its usage policy. For production traffic use an appropriate hosted geocoding service and follow its terms.
- OpenStreetMap tile servers have usage limits; for a high-traffic site use a hosted tile provider.
- Distance is straight-line, not driving distance.
- GitHub Pages is static: accounts, partner self-service editing, SMS alerts, and secure administration require external backend services.
- The demo data is fictional and not suitable for directing people to food assistance.
