# Changelog

## v2.3.0-beta2

### Correzioni

**Pannello Allarme Gold**
- Corretto lo stato che tornava a "disattivato" dopo 10 secondi
- Il pannello ora legge lo stato dalla cache WebSocket (`g1`, `g2`, `g3`)

**Sensori Radio Gold**
- Corretta la mancata visualizzazione dei sensori radio in Home Assistant
- Corretta la propagazione del callback `async_add_entities`
- Corretto il recupero di `user_code` dalla configurazione

### Miglioramenti

**Config Flow**
- Nascosti i campi `num_filari` e `num_radio` per il brand Gold

---

## v2.3.0-beta1

- Supporto iniziale WebSocket Gold
- Refactoring API comune
