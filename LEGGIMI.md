# nembo 1.0.0

Web app meteo di **nautargo**: previsioni, tempo passato dal 1940, pagella delle previsioni, registro con esportazione Excel e PDF, allerte della Protezione Civile.

## Pubblicazione su GitHub Pages

1. Crea il repository `Nembo` (pubblico) sull'account `imo09`.
2. Carica **tutti** i file di questa cartella nella radice del repository, compresi `.nojekyll`, `sw.js`, `manifest.webmanifest` e la cartella `icons`.
3. Settings > Pages > Source: "Deploy from a branch", ramo `main`, cartella `/ (root)`.
4. Settings > Pages > Custom domain: `nembo.nautargo.com`, poi spunta "Enforce HTTPS" quando diventa disponibile.
5. Su Aruba, nel DNS di nautargo.com: record **CNAME** `nembo` che punta a `imo09.github.io`.

Non servono chiavi, account o server: l'app chiama direttamente i servizi aperti.

## Fonti dei dati

- Open-Meteo.com (CC BY 4.0): previsioni, giorni passati, previsioni archiviate, ricerca dei luoghi
- Copernicus ERA5 tramite Open-Meteo: tempo passato dal 1940
- Dipartimento della Protezione Civile (CC BY 4.0): bollettino di criticità nazionale, da GitHub `pcm-dpc`
- GeoNames (CC BY 4.0) per la ricerca, OpenStreetMap per il nome della posizione
