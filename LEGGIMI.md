# nembo 1.1.0

Web app meteo di **nautargo**: previsioni, tempo passato dal 1940, pagella delle previsioni, registro con esportazione Excel e PDF, allerte della Protezione Civile.

## Pubblicazione su GitHub Pages

1. Crea il repository `Nembo` (pubblico) sull'account `imo09`.
2. Carica **tutti** i file di questa cartella nella radice del repository, compresi `.nojekyll`, `sw.js`, `manifest.webmanifest` e la cartella `icons` (le icone devono stare dentro `icons/`, non nella radice).
3. Settings > Pages > Source: "Deploy from a branch", ramo `main`, cartella `/ (root)`.
4. Settings > Pages > Custom domain: `nembo.nautargo.com`, poi spunta "Enforce HTTPS" quando diventa disponibile.
5. Su Aruba, nel DNS di nautargo.com: record **CNAME** `nembo` che punta a `imo09.github.io`.

Non servono chiavi, account o server: l'app chiama direttamente i servizi aperti.

## Fonti dei dati

- Open-Meteo.com (CC BY 4.0): previsioni, giorni passati, previsioni archiviate, ricerca dei luoghi
- Copernicus ERA5 tramite Open-Meteo: tempo passato dal 1940, media climatica 1991-2020
- Copernicus CAMS tramite Open-Meteo: qualità dell'aria
- Dipartimento della Protezione Civile (CC BY 4.0): bollettino di criticità nazionale, da GitHub `pcm-dpc`
- GeoNames (CC BY 4.0) per la ricerca, OpenStreetMap per il nome della posizione

## Novità della 1.1.0

- Layout per tablet e computer: sezioni in alto, Oggi su due colonne, fino a 3 luoghi affiancati (gruppo fissabile da Luoghi)
- Riepilogo ridisegnato con la percepita in evidenza; "Adesso, nel dettaglio" si apre toccando il riepilogo, con "Più dati" (bulbo umido, Luna, Sole, CAPE...)
- Prossime ore e prossimi giorni come strisce con legenda fissa a sinistra: cielo, temperatura, mm, probabilità, vento, UV, qualità dell'aria
- Allerta, attenzione e media del periodo come pulsanti piccoli che si aprono; riga sintetica di domani
- Passato: Registro, Pagella, Giorno. Luoghi: stella per il luogo che si apre all'avvio
- Impostazioni: sottosezioni Guida (definizioni) e Fonti dei dati
- Nuovo logo con la "o" a nuvola
