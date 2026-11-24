# Cleyra

App (iOS, Android, Web) für kleine Schweizer Reinigungsfirmen: Agenda + Rechnungen, maximal einfach.

Prima di ogni compito leggi:
- @docs/PRODUCT.md — cosa fa l'app, cosa c'è nell'MVP e cosa NO
- @docs/DECISIONS.md — decisioni già prese (non riproporre ciò che è stato scartato)
- @docs/ROADMAP.md — a che punto siamo e qual è il prossimo passo

## Come lavoriamo
1. **Prima il piano, poi il codice.** Spiega come lo faresti e aspetta il mio ok.
2. **Un compito alla volta.** Fai solo quello che ho chiesto. Niente funzioni extra, niente "già che c'ero".
3. **Non toccare parti non richieste.** Se pensi che serva, chiedimelo prima.
4. **Alla fine spiegami in parole semplici** cosa hai cambiato e cosa potrebbe rompersi.
5. **Non dire "fatto" senza averlo verificato** (build, test, prova reale).
6. **A fine sessione aggiorna docs/ROADMAP.md.**
7. Parla con me in italiano. Codice, commenti e nomi in inglese.

## Regole fisse del prodotto
- **Un solo codice per iOS, Android e web** con Expo (React Native) ed Expo Router. L'app deve sembrare nativa al 100% sul telefono.
- **Layout responsive:** sul telefono barra in basso; su schermo grande (PC) menu laterale e contenuto più largo. Ogni schermata va provata su telefono E su web.
- **Logica importante sul server, separata dalle schermate:** PDF, QR-bill, fatture fisse automatiche e invio notifiche stanno sul server (Supabase Edge Functions; se Typst non gira lì, un piccolo servizio separato). Le schermate le chiamano soltanto.
- **Notifiche native** con Expo Notifications (APNs per iOS, FCM per Android).
- **Il sito di presentazione (marketing) NON fa parte di questo progetto.**
- **Multi-tenant:** ogni tabella con dati di una ditta ha `company_id`. Row Level Security su TUTTE le tabelle. Una ditta non vede MAI i dati di un'altra.
- **Niente testi scritti nel codice:** ogni testo dell'interfaccia passa dai file di traduzione (de, fr, it, pt, sq).
- **Documenti (fatture) in de / fr / it**, con template separati per lingua.
- **Formati svizzeri:** CHF, arrotondamento a 0.05, date 24.11.2026, niente "ß" nel tedesco.
- **Niente "Mirdita" nel codice:** nome, logo, dati e testi vengono dalle impostazioni della ditta.
- **Semplicità:** azioni quotidiane in massimo 3 tocchi, nessuna parola da contabile, una schermata = un compito, mobile-first.

## Qualità
- **Test (Vitest) obbligatori prima del codice** per: importi e arrotondamenti, QR-bill, separazione dati tra ditte, fatture fisse automatiche.
- Mai salvare chiavi o password nel codice: solo in `.env.local`.

## Tecnologia
Expo (React Native) + Expo Router · TypeScript · NativeWind (Tailwind per React Native) · Supabase (Auth, Postgres, Storage, Edge Functions) · i18next + expo-localization · Expo Notifications · Typst per i PDF (sul server) · Swiss QR-bill · EAS Build per iOS/Android · web export per il PC
