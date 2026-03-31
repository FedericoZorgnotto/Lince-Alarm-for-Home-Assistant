# Changelog

## v2.3.0-beta2

### Correzioni

**Pannello Allarme Gold**
- Corretto lo stato che tornava a "disattivato" dopo 10 secondi
- Il pannello ora legge lo stato dalla cache WebSocket (`g1`, `g2`, `g3`)
- **Corretto flusso ARMING**: ora mostra l'animazione "arming" durante l'inserimento
- Le notifiche vengono inviate quando il WebSocket conferma lo stato

**Sensori Radio Gold**
- Corretta la mancata visualizzazione dei sensori radio in Home Assistant
- Corretta la propagazione del callback `async_add_entities`
- Corretto il recupero di `user_code` dalla configurazione
- **Fix critico**: corretto il percorso di lettura del codice utente (`systems_config` invece di `systems`)
- **Fix reload**: l'integrazione ora si ricarica automaticamente quando il codice utente viene modificato

### Miglioramenti

**Config Flow**
- Nascosti i campi `num_filari` e `num_radio` per il brand Gold
- **Aggiunto campo "Codice Utente Gold" nel login cloud** (opzionale)
  - Permette di caricare i sensori radio/filari fin dalla prima configurazione
  - Senza codice si vede solo lo stato della centrale
  - Il codice può essere aggiunto anche dopo dalla configurazione
- **Controllo duplicati**: impedisce di creare configurazioni duplicate
  - Cloud: stessa email → bloccato
  - Locale: stesso IP:porta → bloccato

---

## v2.3.0-beta1

- Supporto iniziale WebSocket Gold
- Refactoring API comune
