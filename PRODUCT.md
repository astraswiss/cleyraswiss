# Cleyra — Prodotto

## Cos'è
Un'app per piccole ditte di pulizia in Svizzera (1–20 persone).
App vera per iPhone e Android (App Store e Google Play) e web app sul PC. Un solo codice.

**Promessa:** «Agenda und Rechnungen für Reinigungsfirmen. So einfach, dass du keine Anleitung brauchst.»

**Per chi:** titolari bravissimi nel lavoro, per cui l'amministrazione (fatture svizzere, QR, documenti in tedesco/francese) è un peso. Oggi usano Word, Excel o dipendono da un parente o dal fiduciario.

**Perché noi e non bexio / Magic Heidi:**
- fatta solo per ditte di pulizia (agenda + fatture insieme)
- l'app nella lingua del titolare, le fatture nella lingua del cliente
- così semplice che non serve spiegarla

**Primo cliente:** Mirdita Reinigung (Naters).

## MVP — cosa c'è dentro

### 1. Firma (impostazioni ditta)
- Nome, logo, indirizzo, telefono, email
- IBAN per QR-bill, IVA sì/no (+ numero IVA e aliquota)
- Termine di pagamento predefinito (es. 30 giorni)
- Lingua predefinita delle fatture
- Configurazione guidata al primo accesso: massimo 5 minuti

### 2. Kunden (clienti)
- Nome / ditta, indirizzo, telefono, email, note
- **Lingua delle fatture** per cliente: de / fr / it
- Ricerca veloce

### 3. Agenda (semplice)
- Schermata **Heute**: i lavori di oggi, in ordine di ora
- Vista settimana come lista per giorno
- Lavoro: cliente, data, ora, indirizzo (preso dal cliente, modificabile), servizio, prezzo, note
- Lavori ripetuti (ogni settimana / ogni mese)
- Promemoria con notifica nativa
- Pulsante **Erledigt** → crea la fattura già compilata

### 4. Rechnungen (fatture)
- Creata da un lavoro (Erledigt) o da zero
- PDF con Swiss QR-bill, logo e dati della ditta, nella lingua del cliente
- Numero progressivo, data, scadenza, voci, IVA se attiva
- Invio con **Condividi** (WhatsApp / email del telefono, PDF allegato)
- Stato: offen / bezahlt / überfällig (automatico dopo la scadenza)
- Lista "non pagate" sempre visibile

### 5. Fatture fisse (clienti con contratto)
- Per un cliente: importo, descrizione, giorno del mese
- Il giorno stabilito la fattura viene **creata in automatico**
- Il titolare riceve una notifica e la invia con un tocco

### 6. Lingue
- **App:** Deutsch, Français, Italiano, Português, Shqip — ogni utente sceglie la sua
- **Fatture:** Deutsch, Français, Italiano — scelte per cliente

### 7. Base
- Login con email
- Ogni ditta vede solo i suoi dati
- Esportazione dati (CSV) per la ditta e il suo fiduciario
- App iOS e Android con notifiche native (Mergim la prova con TestFlight prima della pubblicazione)

## Fuori dall'MVP (NON costruire)
Vedi la lista "Dopo" in docs/ROADMAP.md.

## Quando l'MVP è finito
Mergim usa Cleyra **per un mese** per agenda e fatture di Mirdita, senza tornare alla vecchia app.
