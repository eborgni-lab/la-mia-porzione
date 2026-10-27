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

- **Pasto**: si sceglie toccando un'icona (🥣 colazione, 🍎 spuntino, 🍝 pranzo, 🥪 merenda, 🍲 cena, 🍗 cena con carne); il nome compare sotto.
- **Note per me** (sempre disponibili, con qualsiasi fonte): per esempio "mangerò anche una mela" (viene conteggiata e la porzione si adatta) o "non mi piace l'aglio" (l'ingrediente viene tolto o sostituito).

- **Testo** (prima scelta): una ricetta incollata oppure un'idea scritta al momento.
- **Foto**: una o più pagine della ricetta (fotocamera o galleria).
- **Testo**: una ricetta incollata, oppure un'idea scritta al momento ("pasta e piselli come la fa la nonna"): l'app crea una ricetta semplice.
- **Pagina web**: incolla il link della ricetta. L'app chiede a Gemini di leggere la pagina; se non ci riesce prova con il servizio gratuito r.jina.ai (che riceve solo l'indirizzo della pagina). Se nessuno dei due funziona, copia il testo e usa la scheda Testo.
- **Versione vegetariana** (attiva di default): carne, salumi e pesce vengono sostituiti con alternative con latte e uova. Si disattiva da sola scegliendo "Cena con carne".
- **Esportare**: "Condividi" su una ricetta apre il menu di condivisione dell'iPhone (Note, Messaggi, Mail, WhatsApp…). "Esporta tutte" crea il file `Le mie ricette.html`, che si apre in qualsiasi browser, si stampa e si può copiare in Word.

## Note

- Il piano gratuito di Gemini usa i dati inviati per migliorare i prodotti Google: non fotografare documenti con dati personali.
- Il modello predefinito è `gemini-flash-latest`; se Google lo cambia, si modifica dalla rotellina in alto (campo Modello).
- Obiettivi: circa 2030 kcal/giorno (ragazza di 15 anni, 1,62 m, peso di riferimento 53 kg = mediana OMS per altezza ed età, attività sedentaria), ripartiti 20/5/35/10/30 tra i pasti. Se il profilo cambia, l'app va rigenerata.
- Valori nutrizionali: tabelle CREA (alimentinutrizione.it) per 17 alimenti principali; per gli altri, medie da tabelle CREA, BDA e USDA.
- "Idea di oggi": un messaggio al giorno da una raccolta tratta da fonti istituzionali e peer review (Linee guida CREA 2018, OMS, SINU), riformulato da Gemini senza aggiungere contenuti. La fonte è sempre indicata. "Questa settimana prova" propone un cereale, un legume, una verdura e un frutto di stagione: toccandoli si prepara una ricetta con quell'ingrediente.
- Le ricette salvate restano solo sul telefono.
