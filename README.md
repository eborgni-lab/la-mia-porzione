# La mia porzione

App web (da aggiungere alla schermata Home dell'iPhone) che legge una ricetta da foto o testo e la riproporziona sul pasto scelto, senza mostrare numeri nutrizionali.

## Pubblicazione su GitHub Pages

1. Crea un nuovo repository (ad esempio `la-mia-porzione`) e carica questi file nella cartella principale:
   `index.html`, `manifest.webmanifest`, `icon-180.png`, `icon-192.png`, `icon-512.png`.
2. Nel repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, scegli il branch `main` e la cartella `/ (root)`, poi **Save**.
3. Dopo un minuto la pagina è online all'indirizzo `https://TUONOME.github.io/la-mia-porzione/`.

## Chiave Gemini (una volta sola)

1. Su un computer, vai su https://aistudio.google.com/apikey con il tuo account Google (serve un adulto) e crea una chiave.
2. Consigliato: nella Google Cloud Console, alla voce della chiave, imposta la restrizione **Siti web (HTTP referrer)** con `https://TUONOME.github.io/*`. Così la chiave funziona solo dalla tua pagina.
3. Sul telefono della ragazza apri l'indirizzo della pagina in Safari: al primo avvio compare la schermata di impostazione. Incolla la chiave e premi **Salva**. Resta salvata solo su quel telefono.

## Installazione sull'iPhone

In Safari: pulsante **Condividi → Aggiungi alla schermata Home**. L'app si apre a schermo intero come un'app normale.

## Come si usa

- **Foto**: una o più pagine della ricetta (fotocamera o galleria).
- **Testo**: una ricetta incollata, oppure un'idea scritta al momento ("pasta e piselli come la fa la nonna"): l'app crea una ricetta semplice.
- **Pagina web**: incolla il link della ricetta. L'app chiede a Gemini di leggere la pagina; se non ci riesce prova con il servizio gratuito r.jina.ai (che riceve solo l'indirizzo della pagina). Se nessuno dei due funziona, copia il testo e usa la scheda Testo.
- **Versione vegetariana** (attiva di default): carne, salumi e pesce vengono sostituiti con alternative con latte e uova. Si disattiva da sola scegliendo "Cena con carne".
- **Esportare**: "Condividi" su una ricetta apre il menu di condivisione dell'iPhone (Note, Messaggi, Mail, WhatsApp…). "Esporta tutte" crea il file `Le mie ricette.html`, che si apre in qualsiasi browser, si stampa e si può copiare in Word.

## Note

- Il piano gratuito di Gemini usa i dati inviati per migliorare i prodotti Google: non fotografare documenti con dati personali.
- Il modello predefinito è `gemini-flash-latest`; se Google lo cambia, si modifica dalla rotellina in alto (campo Modello).
- I dati nutrizionali e gli obiettivi dei pasti sono quelli del file Excel (ragazza, 15 anni, 60 kg, attività sedentaria, 2169 kcal/giorno). Se il profilo cambia, l'app va rigenerata.
- Le ricette salvate restano solo sul telefono.
