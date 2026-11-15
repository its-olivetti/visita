# Controlli Fase 3 — esito pagina per pagina

Verifica eseguita sui file del sito, con gli stessi controlli elencati nella
Fase 3. Data: 13/11/2026.

## 1. Controlli per ogni pagina

| Pagina | `<h1>` | Parole intro (max 25) | Immagini con `alt` | `[MODIFICA]` residui | Data aggiornamento | Pulsante mappa | Presente nella mappa |
|---|---|---|---|---|---|---|---|
| `index.html` | 1 | 24 | — (nessuna immagine) | 0 | 13/11/2026 | — (è la mappa) | — |
| `spazi/aula-n1/` | 1 | 20 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 1) |
| `spazi/aula-n2/` | 1 | 17 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 2) |
| `spazi/aula-n3/` | 1 | 22 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 3) |
| `spazi/aula-n4/` | 1 | 16 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 4) |
| `spazi/aula-n5/` | 1 | 14 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 5) |
| `spazi/aula-n6/` | 1 | 16 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 6) |
| `spazi/porta-aula/` | 1 | 15 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 7) |
| `spazi/porta-bw/` | 1 | 18 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 8) |
| `spazi/porta-ingresso/` | 1 | 21 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 9) |
| `spazi/porta-ufficio/` | 1 | 17 | 1 di 1 | 0 | 13/11/2026 | sì | sì (Spazio 10) |
| `spazi/_template/` | 1 | — (segnaposto) | esempio | sì, per progetto | — | sì | no, per progetto |

Il solo file con `[MODIFICA]` è `spazi/_template/index.html`: è il modello, deve
restare così. Nessuna pagina pubblicata contiene `[MODIFICA]`, `NOME` o
`CODICEVIDEO`.

## 2. Regole di scrittura verificate

| Regola | Esito |
|---|---|
| Niente "Clicca qui" | OK: il pulsante dice "Torna alla mappa degli spazi" |
| Sigle spiegate alla prima occorrenza | OK: ITS Academy (istituto tecnico superiore) in aula-n1, n2, n5, n6, porta-aula, porta-ufficio; GDPR (regolamento europeo…); IoT (Internet of Things); AI (intelligenza artificiale) |
| Paragrafi di 2-3 frasi | OK: i testi della Fase 1 sono stati divisi in paragrafi brevi, senza cambiare le parole |
| Titoli che dicono dove sei | OK: la riga sotto il titolo indica sempre lo spazio fisico e il colore (es. "Aula QR n.1 · colore rosso") |
| Niente tutto maiuscolo | OK: il nome dell'istituto non è più in maiuscoletto forzato (tolto `text-transform: uppercase` dal CSS) e i segnaposto usano "Aula QR n.1 - Rosso" |
| Parole inglesi con `lang="en"` | OK: learning by doing, project management, project work, problem solving, teamworking, policy, cloud, brainstorming, challenge, Cybersecurity Specialist |

## 3. Controlli tecnici eseguiti

- Tutti i link interni e tutte le `src` delle immagini puntano a file esistenti
  (unica eccezione voluta: il percorso generico del template).
- CSS: parentesi bilanciate, nessuna variabile o classe usata e non definita.
- Resa a 390 px di larghezza: nessuno scorrimento orizzontale, nessun elemento
  che esce dallo schermo.
- Un solo `<h1>` per pagina; `<h2>` solo dentro i blocchi video.
- Ogni pagina ha `<html lang="it">`, `viewport`, `<title>` e `description`.

## 4. Punti aperti, per scelta

Sono gli unici due controlli non chiusi, come concordato:

1. **Immagini segnaposto** — le foto non sono ancora disponibili. Le 10 immagini
   in `img/<slug>/` sono segnaposto colorati con la scritta "Immagine
   segnaposto": vanno sostituite mantenendo lo stesso nome file (istruzioni nel
   README, sezione 5).
2. **Blocchi video commentati** — nessun video è pronto. Ogni pagina contiene il
   blocco video pronto ma dentro un commento HTML, quindi non compare ai
   visitatori. Se un video non servirà, il blocco va cancellato per intero.

Quando le foto e i video saranno definitivi, questi due punti si chiudono e la
checklist della Fase 3 risulta completa al 100%.
