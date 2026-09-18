# Grangia GSAP Immersive

Esperienza web immersiva derivata dalla presentazione **“Grangia x 40 anni.pptx”**.

La sequenza conserva i contenuti principali delle 24 slide originali e li presenta con un linguaggio visivo volutamente neutro. Le sole eccezioni cromatiche sono i quattro foglietti di riflessione. L’unica fotografia utilizzata è quella della Grangia, trattata in scala di grigi nelle schermate di apertura, accoglienza e chiusura.

## Avvio

Il progetto non richiede build né dipendenze da installare. È incluso un piccolo server statico Node.js.

- Windows: esegui `start.bat`.
- macOS/Linux: esegui `./start.sh`.
- Da terminale: `npm start`.
- In alternativa, avvia un qualsiasi server statico nella cartella e apri `index.html` tramite HTTP.

GSAP è incluso localmente in `assets/vendor/gsap.min.js`, quindi l’esperienza può essere presentata senza connessione internet.

## Funzionamento

- Il pulsante iniziale avvia un conto alla rovescia.
- Le schermate narrative avanzano automaticamente.
- I checkpoint di riflessione avanzano solo dopo il click del partecipante; alcuni prevedono un breve tempo minimo.
- I controlli consentono di mettere in pausa, tornare indietro, andare avanti, uscire e attivare lo schermo intero.
- La pagina finale contiene il pulsante **Ricomincia**.

## Tastiera

- `←` / `→`: schermata precedente o successiva.
- `Spazio`: pausa/riprendi.
- `F`: schermo intero.

## Pubblicazione su GitHub Pages

Il workflow `.github/workflows/pages.yml` pubblica una whitelist dei soli file necessari al sito. PowerPoint, server locale, documentazione e immagini inutilizzate non entrano nell’artefatto pubblico.

Per verificare localmente il contenuto che verrà distribuito:

```bash
npm run build:pages
```

L’output viene creato in `dist-pages/` ed è escluso da Git. Nel repository GitHub, imposta una sola volta **Settings → Pages → Source → GitHub Actions**. Ogni push successivo su `main` avvierà automaticamente la pubblicazione; è possibile avviarla anche manualmente dalla sezione **Actions**.
