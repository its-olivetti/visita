# Visita il Centro Adriano Olivetti — Fase 2 e Fase 3

Sito statico con la mappa degli spazi e una pagina per ogni QR code definito
nella Fase 1. Funziona senza internet: basta aprire `index.html` con un doppio
clic. Non serve alcun programma: solo HTML e CSS.

## 1. Struttura delle cartelle

```
sito/
├── index.html                        mappa con l'elenco dei 10 spazi
├── README.md                         questo file
├── controlli-fase-3.md               esito dei controlli, pagina per pagina
├── Fase-1.txt / Fase-2.txt / Fase-3.txt   documenti di partenza
├── css/
│   └── stile.css                     unico foglio di stile del sito
├── img/
│   ├── aula-n1/competenze-trasversali.png
│   ├── aula-n2/metodo-learning-by-doing.png
│   ├── aula-n3/proteggere-il-digitale.png
│   ├── aula-n4/analisi-e-prevenzione.png
│   ├── aula-n5/reti-e-infrastrutture.png
│   ├── aula-n6/lavoro-di-squadra.png
│   ├── porta-aula/cybersecurity-e-lavoro.png
│   ├── porta-bw/brain-waves-crittografia.png
│   ├── porta-ingresso/ingresso-centro.png
│   └── porta-ufficio/tutor-e-coordinatori.png
└── spazi/
    ├── _template/index.html          modello da duplicare
    ├── aula-n1/index.html
    ├── aula-n2/index.html
    ├── aula-n3/index.html
    ├── aula-n4/index.html
    ├── aula-n5/index.html
    ├── aula-n6/index.html
    ├── porta-aula/index.html
    ├── porta-bw/index.html
    ├── porta-ingresso/index.html
    └── porta-ufficio/index.html
```

I nomi delle cartelle sono gli slug scelti nella Fase 1: **non cambiarli** dopo
aver stampato i QR, perché l'URL dipende da quei nomi.

Le immagini attuali sono segnaposto colorati (1200 × 800 px): vanno sostituite
con le foto vere, mantenendo lo stesso nome del file oppure aggiornando `src`
nella pagina.

## 2. Corrispondenza con la Fase 1

| N. | Spazio | Cartella / slug | Titolo pagina | Colore | Video |
|----|--------|-----------------|---------------|--------|-------|
| 1 | Aula | `spazi/aula-n1/` | Le competenze che non si vedono, ma fanno la differenza | rosso | previsto |
| 2 | Aula | `spazi/aula-n2/` | Dalla teoria alla pratica: il metodo learning by doing | blu | previsto |
| 3 | Aula | `spazi/aula-n3/` | Proteggere il digitale | viola | previsto |
| 4 | Aula | `spazi/aula-n4/` | Non solo attacchi: analisi, prevenzione e risposta | viola | previsto |
| 5 | Divisore Aula | `spazi/aula-n5/` | Reti, sistemi e infrastrutture digitali | blu | previsto |
| 6 | Divisore Aula | `spazi/aula-n6/` | Collaborare è una competenza tecnica | rosso | previsto |
| 7 | Porta Aula | `spazi/porta-aula/` | Cybersecurity: un settore che cambia il mondo del lavoro | rosa | previsto |
| 8 | Porta BW | `spazi/porta-bw/` | Brain Waves: dove la crittografia diventa ricerca | rosso | sì (Fase 1) |
| 9 | Porta Ingresso | `spazi/porta-ingresso/` | Benvenuto nel Centro di Innovazione e Formazione Adriano Olivetti | azzurro | previsto |
| 10 | Porta Ufficio | `spazi/porta-ufficio/` | Un punto di riferimento, sempre | rosso | previsto |

Tutte le pagine hanno `ultimo aggiornamento: 13/11/2026`, come indicato nella
Fase 1. Quando modifichi un contenuto, aggiorna anche quella data.

## 3. Che cosa contiene ogni pagina

Ogni `spazi/<slug>/index.html` è costruito sul modello `spazi/_template/` e
contiene, nell'ordine:

- link "Vai al contenuto" (visibile solo con Tab);
- `<header>` con nome dell'istituto, `<h1>` (uno solo), posizione fisica e colore
  del QR (pallino + colore scritto a parole);
- `<main>` con frase introduttiva (`p.introduzione`, barra colorata a sinistra),
  testo in paragrafi brevi, immagine in `<figure>`, blocco video commentato e
  data di aggiornamento;
- `<footer>` con il pulsante "Torna alla mappa degli spazi"
  (`../../index.html`).

## 4. Regole di scrittura applicate (Fase 3)

| Invece di | Nel sito |
|---|---|
| "Clicca qui" | "Torna alla mappa degli spazi" |
| Sigle senza spiegazione | "ITS Academy (istituto tecnico superiore)", "GDPR (regolamento europeo sulla protezione dei dati personali)", "IoT (Internet of Things, gli oggetti connessi)" |
| Paragrafi di 10 righe | Paragrafi di 2-3 frasi |
| Titoli creativi | Sotto il titolo c'è sempre lo spazio fisico: "Aula QR n.1 · colore rosso" |
| Tutto maiuscolo | Maiuscole normali (tolto anche il maiuscoletto forzato del CSS) |
| Parole inglesi senza lingua | `<span lang="en">learning by doing</span>`, così lo screen reader le pronuncia bene |

Quando aggiungi testo:

- spiega ogni sigla alla prima occorrenza nella pagina;
- chiudi le parole inglesi in `<span lang="en">…</span>`;
- tieni la frase introduttiva entro 25 parole;
- niente email, telefoni, nomi di studenti, orari o informazioni sulla sicurezza.

## 5. Come modificare una pagina

1. Apri il file `spazi/<slug>/index.html` con un editor di testo (Blocco note,
   Notepad++, VS Code).
2. Salva in **UTF-8** (le lettere accentate altrimenti si rovinano).

### Sostituire una foto

1. Metti il file in `img/<slug>/` (stesso nome della cartella in `spazi/`).
2. Nella pagina aggiorna `src`, `alt`, `width` e `height`.
3. `width` e `height` devono essere le misure reali dell'immagine: evitano che la
   pagina "salti" durante il caricamento.
4. `alt` descrive ciò che si vede, non "foto 1". Se l'immagine è solo
   decorativa, usa `alt=""`.
5. Formato consigliato: JPG o WebP, lato lungo max 1600 px, sotto 300 KB.

Se la foto non serve, cancella tutto il blocco `<figure>` (dal tag di apertura a
`</figure>` compreso).

### Attivare un video

Ogni pagina ha già il blocco video pronto, ma commentato: così la pagina
funziona anche senza video.

1. Nel file cerca `inizio video` e `fine video`.
2. Togli la riga di commento che apre il blocco e quella che lo chiude (le righe
   che iniziano con `<!--` e finiscono con `-->`).
3. Sostituisci ogni `VIDEO_ID` con l'identificativo YouTube (la parte dopo `v=`
   nell'indirizzo del video).
4. Scrivi la trascrizione dentro `<details>`.

Il video usa `youtube-nocookie.com`, non parte da solo, ha un `title` per gli
screen reader, un link di riserva e la trascrizione. Se il video non servirà,
cancella il blocco per intero, come chiede la checklist della Fase 3.

### Duplicare una pagina per un nuovo spazio

1. Copia la cartella `spazi/_template` e rinominala con il nuovo slug.
2. Apri il nuovo `index.html` e cambia i punti `[MODIFICA]`.
3. Aggiungi il nuovo `<li>` nella mappa `index.html`.
4. Crea `img/<nuovo-slug>/` e mettici le foto.

## 6. Il CSS: le scelte principali

- Font di sistema, 20 px (impostati come `125%` sulla radice, quindi rispettano
  l'ingrandimento del telefono) e interlinea 1,6.
- Colonna larga al massimo `40rem`: su tablet e computer il testo non diventa
  illeggibilmente lungo.
- Contrasto: nero su bianco ≈ 17:1, bianco sul blu dei pulsanti ≈ 8,5:1 (minimo
  richiesto 4,5:1).
- Pulsanti alti almeno `3.5rem` e distanziati, per evitare tocchi sbagliati.
- Contorno di focus sempre visibile per chi naviga con la tastiera.
- Nessuna animazione; se il sistema chiede movimento ridotto, non cambia nulla.
- Colori modificabili in cima al file, nel blocco `:root`. Se cambi il blu dei
  pulsanti o il colore di sfondo, ricontrolla il contrasto su
  <https://webaim.org/resources/contrastchecker/> (gratuito).

## 7. Il sito è online (GitHub Pages)

- Repository: <https://github.com/its-olivetti/visita> (pubblico)
- Sito: <https://its-olivetti.github.io/visita/>
- Pubblicazione: ramo `main`, cartella `/ (root)`, rebuild automatico a ogni push
- Elenco degli indirizzi per i QR: `url-qr.txt`

### Aggiornare il sito

Dopo aver modificato o sostituito file:

```
git add -A
git commit -m "Descrizione della modifica"
git push
```

GitHub Pages ricostruisce in uno o due minuti.

### Maiuscole negli indirizzi

Su GitHub l'indirizzo è sensibile alle maiuscole: `spazi/porta-bw/` funziona,
`spazi/porta-BW/` risponde 404. Per questo, il 15/11/2026, le cartelle sono
state portate tutte in minuscolo (`spazi/porta-bw/` e `img/porta-bw/`), come
era già per gli altri nove spazi.

Non cambiare mai gli slug dopo aver stampato i QR: l'indirizzo è dentro il QR.

## 8. Controlli prima di stampare i QR

L'esito completo è in `controlli-fase-3.md`. Riepilogo:

- [x] Un solo `<h1>` per pagina, che dice il nome dello spazio.
- [x] Frase introduttiva entro 25 parole (da 14 a 24).
- [x] Ogni immagine ha un `alt` utile.
- [x] Nessun `[MODIFICA]`, `NOME` o `CODICEVIDEO` nelle pagine pubblicate.
- [x] Data di aggiornamento corretta in fondo a ogni pagina.
- [x] Il pulsante "Torna alla mappa degli spazi" funziona.
- [x] Tutte le pagine compaiono nella mappa.
- [ ] Foto reali al posto dei segnaposto.
- [ ] Video decisi: attivati o blocco cancellato.
- [ ] Provato su telefono (390 px) e con la tastiera (Tab).
- [ ] Provato con lo zoom al 200%: nessun testo tagliato.

## 9. Avvisi

- Il video YouTube carica script di Google quando si preme play. Per zero
  tracciamento serve un file video leggero ospitato nel sito (Fase 4).
- Tutto ciò che pubblichi è visibile a chiunque su internet, non solo a chi
  scansiona il QR.
- I cinque slug proposti nella Fase 3 (`competenze-trasversali`,
  `competenze-tecniche`, `macro-settore`, `struttura-e-sede`, `corso-specifico`)
  sono l'esempio del corso: non sono stati usati, perché gli indirizzi dei QR
  erano già stati scelti nella Fase 1.
