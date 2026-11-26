# nembo 1.2.1

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
- Modello d'insieme ECMWF (51 scenari) tramite Open-Meteo: attendibilità della previsione
- Copernicus ERA5 tramite Open-Meteo: tempo passato dal 1940, media climatica 1991-2020
- Copernicus CAMS tramite Open-Meteo: qualità dell'aria
- Dipartimento della Protezione Civile (CC BY 4.0): bollettino di criticità nazionale, da GitHub `pcm-dpc`
- GeoNames (CC BY 4.0) per la ricerca, OpenStreetMap per il nome della posizione

## Novità della 1.2.1

- Icone meteo riviste tutte: raggi del sole uniformi e solo dove non toccano la nuvola, gocce, fiocchi e fulmine centrati sotto la nuvola
- In ogni pannello dell'allerta, il collegamento al sito delle allerte della Regione del luogo (per Molise, Puglia e Provincia di Trento, in attesa di un indirizzo verificato, l'elenco nazionale dei Centri Funzionali)
- Icona dell'app e favicon con la "o" di nembo

## Novità della 1.2.0

- Previsione a 14 giorni, con attendibilità in percentuale per ogni ora e ogni giorno (51 scenari ECMWF)
- Prossimi giorni: temperature come due linee (massime e minime), righe sottili ogni 5 gradi in tutti i grafici
- Grafico del giorno: orari più fitti secondo la larghezza dello schermo, con l'icona del cielo sopra ogni orario
- Umidità nelle strisce delle ore e dei giorni e nel giorno ora per ora; tolti i doppioni dal dettaglio; punto di rugiada solo in "Più dati"
- Icone "i" al posto di note e didascalie: cosa indica il dato, cosa comporta, lettura del valore mostrato, e rimando alla guida (riscritta con le stesse voci)
- Icone meteo ridisegnate (bicolori, centrate) e animazioni rifatte; l'icona di Oggi nella barra è il tempo di adesso
- Splash con la "o" di nembo animata, "Tocca per continuare", versione e "by nautargo"; si può disattivare dalle Impostazioni
- Allerta, attenzione e media del periodo chiusi su una sola riga
- Luoghi affiancati: nomi fissi in alto con temperatura, massima e minima; avvertenze e fonti una sola volta
- Passato: layout uniforme, soglia dei giorni di pioggia dentro il riquadro "Giorni di pioggia"
- Protezione Civile: controllo più frequente tra le 13 e le 18 e ricerca dell'ultimo bollettino più robusta
- Tolta la mail di supporto dalle Impostazioni

## Novità della 1.1.0

- Layout per tablet e computer: sezioni in alto, Oggi su due colonne, fino a 3 luoghi affiancati (gruppo fissabile da Luoghi)
- Riepilogo ridisegnato con la percepita in evidenza; "Adesso, nel dettaglio" si apre toccando il riepilogo, con "Più dati" (bulbo umido, Luna, Sole, CAPE...)
- Prossime ore e prossimi giorni come strisce con legenda fissa a sinistra: cielo, temperatura, mm, probabilità, vento, UV, qualità dell'aria
- Allerta, attenzione e media del periodo come pulsanti piccoli che si aprono; riga sintetica di domani
- Passato: Registro, Pagella, Giorno. Luoghi: stella per il luogo che si apre all'avvio
- Impostazioni: sottosezioni Guida (definizioni) e Fonti dei dati
- Nuovo logo con la "o" a nuvola
