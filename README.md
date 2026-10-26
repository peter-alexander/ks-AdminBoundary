# ks-AdminBoundary

Erzeugt zwei Overture-Admin-PMTiles für die Kartensammlung.

- `overture-admin-area.pmtiles` (z11): GitHub Release-Asset.
- `overture-admin-boundary.pmtiles` (z14): Cloudflare R2.

Manueller Build über **Actions → Build Overture AdminBoundary → Run workflow**.

GitHub-Actions-Secrets für R2: `R2_ACCOUNT_ID`, `R2_ACCESS_KEY_ID`, `R2_SECRET_ACCESS_KEY`, `R2_BUCKET`. Die Bucket-Adresse ist nicht der öffentliche Abruf-Endpunkt; für PMTiles-Clients einen öffentlichen R2-Endpunkt mit CORS und Range-Unterstützung konfigurieren.

`release.json` und `audit.json` werden als Build-Artefakte gespeichert.

Die Kartenherstellung nutzt Overture Maps und die Wiener Bezirksgrenzen (Stadt Wien OGD).
