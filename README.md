# 🏎️ F1 Career Simulator

**Gestionale di Formula 1 per PC e telefono.** Costruisci la carriera di un pilota su più stagioni: weekend completo (prove libere, qualifiche, sprint, gara), mappa live, strategie, bandiere, meteo, mercato piloti, sviluppo della vettura, team radio con voce e salvataggi a slot.

**Ultima versione: 2.7.1** · Interfaccia e testi in italiano · radio dell'ingegnere e del pilota in inglese (testo a schermo in italiano)

> Questo repository contiene solo i **rilasci** (download e guida). Il codice sorgente è privato.

---

## 📥 Scarica

Vai in **[Releases](../../releases/latest)** e scegli:

| Dove giochi | Cosa scaricare |
|---|---|
| **PC Windows** | `F1Career_PC_<versione>.zip` |
| **Telefono / qualsiasi browser** | apri la web app (link nella descrizione della release) oppure scarica `F1Career_web.html` |

Le versioni precedenti restano nelle release più vecchie (lo zip PC contiene anche la cartella `versioni_precedenti`).

---

## 🖥️ Gioco su PC (Windows)

**Requisiti**
- Windows 10/11
- Python **3.13**
- Pygame **2.6.1** (il file `avvia_gioco.bat` lo installa da solo se manca)

**Avvio**
1. Estrai **tutto** lo ZIP in una cartella (non avviare da dentro lo ZIP).
2. Doppio clic su `avvia_gioco.bat`. In alternativa: `py -3.13 main.py` (su macOS/Linux: `avvia_gioco.sh`).
3. Dal menu scegli **Nuova carriera**, **Carriera salvata** (elenco di tutti gli slot) oppure **Continua l'ultima**.

Se qualcosa non va, il gioco mostra un messaggio chiaro (file mancante, Pygame assente…) e, in caso di errore, salva la carriera e scrive `f1_crash.log`.

## 📱 Gioco da telefono

La versione mobile è una **web app** (funziona anche su PC, in qualsiasi browser moderno):
- apri il link della web app e usa **Aggiungi a schermata Home** per installarla come app (PWA);
- oppure apri `F1Career_web.html` direttamente nel browser.

I salvataggi vivono **nel browser del dispositivo** (5 slot): usa **Esporta** per farne una copia o passarli a un altro dispositivo. Le voci radio si attivano al primo tocco.

Quando esce una nuova versione compare un avviso: su PC un popup (`INVIO` scarica, `S` salta, `ESC` più tardi), sul telefono un banner con aggiornamento a un tocco.

---

## 🎮 Come si gioca

Una carriera segue questo giro, ogni stagione:

1. **Contratto e sponsor** – firmi con una scuderia e scegli 3 sponsor su 12.
2. **Menu carriera** – sviluppo vettura, monoposto e componenti, pilota e allenamento, mercato, notizie, rivalità, tifosi, interviste.
3. **Weekend di gara** – prove libere → qualifiche (o sprint-quali) → gara, con eventuali eventi e domande dei giornalisti.
4. **Fine stagione** – classifiche, contratti, crescita del pilota, evoluzione delle vetture.

### Qualifiche guidate a mano (novità 2.7.1)
Sei tu a decidere:
- **quando uscire dai box** e con **quali gomme** (Soft/Medium/Hard; Inter/Wet con il bagnato). I set nuovi sono limitati per fase, quando finiscono si monta una gomma usata;
- **quando attaccare**: parte il giro lanciato al prossimo passaggio sul traguardo;
- **quando usare il Boost**: la batteria cala del 3% al secondo, rende sui rettilinei, poco in curva (e in curva può bloccare);
- **quando rientrare**.

Un pannello di aiuto mostra tempo rimasto, ultima uscita utile, posizione, linea di taglio e tempo previsto. In ogni momento puoi dire **«Lascia fare al team»** o saltare al risultato.
**Il tempo parte a 1x (reale)** e puoi cambiare velocità quando vuoi: 1x, 2x, 4x, 8x, 30x.

| Azione | PC | Telefono |
|---|---|---|
| Esci dai box | `E` | pulsante |
| Cambia gomma | `T` | pulsante |
| Attacca | `A` | pulsante |
| Boost | `G` | pulsante |
| Rientra | `R` | pulsante |
| Lascia fare al team | `U` (`ESC` = il team finisce la sessione) | pulsante |
| Meteo | `W` | 🌦 Meteo |
| Audio | `V` | 🔊 Audio |
| Pausa | `SPAZIO` | ⏸ |
| Velocità 1x / 2x / 4x / 8x / 30x | `1`–`5` | pulsanti |
| Dopo ogni fase | `INVIO` continua | pulsante |

### Gara
Strategia (partenza, soste, carburante), modalità di guida (Conservativa / Standard / Aggressiva / Massima), **Boost · ERS · Overtake**, sosta ai box con scelta della mescola, bandiere, Safety Car, Virtual Safety Car, bandiera rossa, penalità e team radio. Alla partenza reagisci allo spegnimento dei semafori: il tuo tempo di reazione conta.

---

## ✨ Funzioni

**Weekend e regole**
- **Qualifiche FIA 2026**: Q1 18' (22→16), Q2 15' (16→10), Q3 12'; sprint-quali SQ1 12' / SQ2 10' / SQ3 8'. Ogni team decide da solo quando uscire, quanti tentativi fare e se rischiare un solo giro finale.
- **Traffico, errori, bandiere**: chi non è sul giro lanciato deve liberare la traiettoria (conta la curvatura reale del circuito); bloccaggi, limiti pista, uscite, testacoda, incidenti, problemi tecnici, gialle, doppie gialle e rosse.
- **Commissari** secondo le regole 2026: avvertimento, richiamo, penalità di posizioni, tempo cancellato, squalifica. Al 5° richiamo stagionale (almeno 4 per pilota) scattano 10 posizioni.
- **Griglia finale** distinta dal risultato delle qualifiche, con tutte le penalità applicate.
- **24 circuiti** con corsia box e garage su ogni pista, sia su PC sia su mobile.

**Meteo**
- **Percentuale di pioggia** sempre visibile in gara e in qualifica (piove / pista bagnata %), con **effetto pioggia** a schermo e **suono della pioggia**.
- Pannello **Meteo** con la **previsione indicativa** a fasce per tutta la qualifica e per tutta la gara, meno affidabile quanto più è lontana nel tempo, come nella realtà.

**Vettura e sviluppo**
- **21 componenti** (power unit, trasmissione, aerodinamica, telaio, freni, ausiliari), ognuno con prestazione, affidabilità, efficienza, peso e usura.
- **Limiti di unità FIA 2026** per pilota e stagione, con penalità automatiche sulla griglia (−10 la prima unità extra, −5 le successive; oltre 15 posizioni si parte dal fondo).
- **Ricerca e sviluppo**: componente, obiettivo (prestazione, affidabilità, efficienza, peso) e pacchetto, con costo, tempo, guadagno e rischio di fallimento.
- **Assetto personalizzabile**: ala anteriore e posteriore, altezza da terra, sospensioni, pressione gomme, bilanciamento freni. Ogni pista ha un assetto ideale nascosto (dipende da tracciato e meteo) e il pilota dà un feedback sempre più preciso dopo ogni prova.
- **Evoluzione del grip** nel weekend: ogni sessione stende gomma sull'asfalto, la pioggia la lava.

**Carriera ed economia**
- **Due budget**: budget scuderia (punti di entrambi i piloti, per vettura e componenti) e budget pilota (solo i tuoi risultati, per l'allenamento personale).
- **12 sponsor** con bonus di gara e di stagione.
- Contratti, mercato piloti, rivalità, tifosi e social, stampa e interviste, crescita del pilota, salvataggi a slot.

**Audio**
- Motore legato alla posizione in pista (basso in curva, alto sui rettilinei), effetti e pioggia.
- **Team radio** con voci clonate (ingegnere e pilota), al massimo 1–2 messaggi per giro. Il pilota risponde raramente e solo «Copy».
- Su mobile, pulsante **Audio** con volumi separati: generale, motore, ingegnere, effetti, pioggia (salvati sul dispositivo). Su PC la schermata Audio si apre con `V`.
- Safety Car, VSC e bandiera rossa hanno suoni più morbidi.

---

## 🗂️ Cartelle dello ZIP PC

```
avvia_gioco.bat        avvio Windows (py -3.13)
avvia_gioco.sh         avvio macOS/Linux
main.py                punto di ingresso
f1sim/                 moduli del gioco (tutti necessari)
assets/                audio del motore e pacchetti voce
fixtures/              salvataggi di prova delle versioni precedenti
versioni_precedenti/   le versioni rilasciate prima
README.md              questa guida
```

## ❓ Problemi frequenti

- **«Python 3.13 non trovato»** – installa Python 3.13 da python.org (spunta *Add to PATH* e il launcher `py`).
- **Il gioco non parte da dentro lo ZIP** – estrai tutto lo ZIP in una cartella.
- **Nessuna voce radio** – su telefono tocca lo schermo una volta; controlla il pulsante 🔊 e i volumi.
- **Ho perso i salvataggi del telefono** – sono nel browser: cancellare i dati del sito li cancella. Esporta una copia ogni tanto.

## ⚠️ Limiti noti

- La voce radio dice «Flag, position N» a fine Q1/Q2/Q3: la parola «chequered» non è nel pacchetto voce attuale.
- Motore e pioggia della versione web sono suoni sintetizzati, non le registrazioni del PC.
- Le previsioni meteo sono indicative.
- Il bilanciamento è calibrato con simulazioni automatiche, non con stagioni giocate a lungo: i numeri possono cambiare nelle prossime versioni.
- La versione telefono non è ancora stata provata su tutti i dispositivi (iPhone/Safari compreso).

---

## 🧾 Cronologia delle versioni

| Versione | Novità principali |
|---|---|
| **2.7.1** | Qualifica guidata a mano (uscita, gomme, attacco, Boost, rientro) con tempo a 1x e velocità selezionabile; meteo con percentuale, effetto e suono della pioggia e previsioni per qualifica e gara; volumi separati su mobile; Safety Car/VSC/bandiera rossa più silenziosi; radio a fine Q1/Q2/Q3; corsia box in tutte le piste |
| **2.7** | Qualifiche FIA 2026 complete con strategie dei team, traffico, commissari e griglia finale; assetto personalizzabile; evoluzione del grip; budget pilota accanto al budget scuderia |
| **2.6.9** | Corsia box e garage su ogni pista (mobile); arrivo dei piloti più rapido |
| **2.6.8** | Due budget (scuderia e pilota), allenamento personale, 12 sponsor |
| **2.6.7** | Nessun team radio nel giro di partenza; suono dei semafori più leggero |
| **2.6.6** | Semaforo di partenza come su PC (mobile) |
| **2.6.5** | Team radio più frequenti; il pilota risponde solo «Copy»; partenza con reazione ai semafori su mobile |
| **2.6.4** | Nuova voce del pilota; arrivo con bandiera a scacchi su mobile |
| **2.6.3** | Boost che aiuta nel sorpasso; pulsanti Boost/ERS/Overtake su mobile; molte schermate in più sul telefono |
| **2.6.2** | Voci radio clonate (RVC) per ingegnere e pilota |
| **2.6.1** | Frasi radio intere al posto dei pezzi |
| **2.6** | Schermata Monoposto: 21 componenti, limiti FIA 2026, ricerca e sviluppo |
| **2.5.x** | Contratto e sponsor, tifosi e stampa, sviluppo vettura, crescita pilota, team radio rivisti, motore legato alle curve |
| **2.0 – 2.4** | Carriera multi-stagione, weekend completo, mercato, bandiere e Safety Car, eventi, salvataggi a slot |

---

## 📝 Segnalazioni

Hai trovato un errore o hai un'idea? Apri una **[Issue](../../issues)** e scrivi: versione, dispositivo (PC o telefono e browser), cosa stavi facendo e cosa è successo.

*Progetto indipendente e non ufficiale: non è affiliato né approvato da Formula 1, FIA o dalle scuderie.*
