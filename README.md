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

## Servizio di riserva (facoltativo): OpenRouter

1. Crea un account gratuito su https://openrouter.ai e una chiave su https://openrouter.ai/keys (non serve la carta di credito).
2. Nella rotellina dell'app incolla la chiave nel campo **Riserva** e premi **Salva**. Con **Prova la connessione** verifichi che sia valida.
3. L'app usa OpenRouter solo se Gemini è sovraccarico (errore 503), ha raggiunto i limiti (429) o non risponde. Sceglie da sola tra i modelli gratuiti disponibili in quel momento, con lettura delle foto se servono.
4. Limiti dei modelli gratuiti: 20 richieste al minuto e 50 al giorno (1000 al giorno dopo un acquisto una tantum di 10 crediti).
5. I modelli gratuiti di OpenRouter sono offerti da fornitori diversi, che possono conservare i dati inviati: vale la stessa regola di Gemini, niente dati personali nelle foto.

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
- Modello: con «auto» (consigliato) l'app chiede a Google quali modelli sono disponibili per la chiave e usa il Flash stabile più recente. Se un modello viene ritirato, passa da sola al successivo.

## Spesa e alimenti non graditi

- **🛒 Spesa**: "Prepara la lista della settimana" chiede a Gemini una lista per una persona, con verdura e frutta di stagione, almeno 3 cereali e 2 legumi diversi, latticini, uova, una porzione di carne, frutta secca. Le quantità sono indicative (porzioni standard LARN e frequenze delle Linee guida CREA). Ogni voce si spunta mentre si fa la spesa; "Condividi la lista" la manda a Note, Promemoria o WhatsApp. Ogni nuova lista evita di ripetere gli alimenti principali delle due settimane precedenti.
- **🚫 Non mi piace**: gli alimenti inseriti qui non compaiono né nella lista della spesa né nelle ricette (vengono tolti o sostituiti).

## Composizione del piatto

- A pranzo e a cena, se la ricetta contiene poca verdura, l'app aggiunge sempre un contorno di stagione (insalata, pomodori, broccoli o finocchi) prima di altri accompagnamenti.
- La porzione del piatto principale non viene ingrandita più del 10%: l'energia mancante arriva da contorno, pane, frutta o yogurt.
- Gli ingredienti minori (aglio, erbe, spezie) mantengono la quantità indicata nella ricetta.

## Velocità

- L'app chiede a Gemini di ragionare poco (livello di "pensiero" basso), che riduce molto i tempi di risposta.
- Nella rotellina: **Modalità veloce** usa il modello Flash-Lite, ancora più rapido ma un po' meno preciso con le foto.
- Sempre nella rotellina compare la durata dell'ultima richiesta e il modello usato.

## Se qualcosa non funziona

1. Rotellina in alto → **Prova la connessione**: dice se la chiave è valida e quale modello verrà usato.
2. Nei messaggi di errore tocca **Dettagli tecnici**: compare il codice (es. 404 modello non trovato, 429 troppe richieste, 503 Gemini sovraccarico) con il messaggio di Google.
3. Da computer puoi vedere i modelli disponibili aprendo `https://generativelanguage.googleapis.com/v1beta/models?key=LA_TUA_CHIAVE` (poi cancella la cronologia, perché contiene la chiave).
- Obiettivi: circa 2030 kcal/giorno (ragazza di 15 anni, 1,62 m, peso di riferimento 53 kg = mediana OMS per altezza ed età, attività sedentaria), ripartiti 20/5/35/10/30 tra i pasti. Se il profilo cambia, l'app va rigenerata.
- Valori nutrizionali: tabelle CREA (alimentinutrizione.it) per 17 alimenti principali; per gli altri, medie da tabelle CREA, BDA e USDA.
- "Idea di oggi": un messaggio al giorno da una raccolta tratta da fonti istituzionali e peer review (Linee guida CREA 2018, OMS, SINU), riformulato da Gemini senza aggiungere contenuti. La fonte è sempre indicata. "Questa settimana prova" propone un cereale, un legume, una verdura e un frutto di stagione: toccandoli si prepara una ricetta con quell'ingrediente.
- Le ricette salvate restano solo sul telefono.
