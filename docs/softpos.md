# Soluzione SoftPOS Nexi & Custom Pay
## L'Ecosistema Unificato per i Pagamenti Digitali

L'integrazione tra i dispositivi Android serie EDGE (**modello N+**) e i servizi di acquiring **Custom Pay / Nexi** rappresenta un'evoluzione architetturale del punto cassa. 
Registratore telematico, gestionale di vendita e terminale di pagamento convergono in un unico dispositivo hardware, eliminando la necessità di POS fisici esterni e semplificando la gestione tecnica e contabile.

---

## 1. Architettura della Soluzione (SoftPOS)

La tecnologia SoftPOS (Software Point of Sale) trasforma l'EDGE N+ in un vero e proprio terminale di pagamento contactless.

* **Requisito Hardware:** Antenna NFC integrata (presente nativamente su EDGE N+).
* **Requisito Software:** Sistema operativo Android 13 con supporto GMS (Google Mobile Services) e aggiornamenti OTA per garantire i massimi standard di sicurezza richiesti dai circuiti bancari.
* **Flusso Operativo:** L'importo viene passato direttamente dall'applicativo di cassa (es. KeepUp Smart) all'App SoftPOS Nexi. Il cliente avvicina la carta o lo smartphone (Apple Pay/Google Pay) al display dell'EDGE N+ per concludere la transazione.


---

## 2. I Vantaggi della Convenzione Custom Pay

Custom Pay opera come intermediario unico, ottimizzando l'intera filiera dell'onboarding e della gestione per l'esercente.

### Unico Interlocutore
* **Semplificazione:** Hardware, software di cassa, fiscalità e gestione transata sono supportati da un solo ecosistema.
* **Assistenza Centralizzata:** In caso di anomalie di comunicazione tra cassa e pagamenti, il dealer e l'esercente si rivolgono a un unico servizio di supporto (Portale Operations/Ticket Custom).

### Gestione Finanziaria Trasparente
* **Nessun Nuovo Conto Corrente:** Non è richiesta l'apertura di un conto dedicato. Le transazioni vengono accreditate direttamente sull'IBAN esistente dell'esercente (modificabile in qualsiasi momento senza rifare il contratto).
* **Tempistiche di Accredito Rapide:** Conformemente al D. Lgs. 11/2010, la data valuta dell'accredito sul conto dell'esercente avviene tipicamente entro la giornata operativa successiva all'operazione.

### Circuiti Supportati (Acquiring Nexi)
La convenzione garantisce la massima copertura dei principali circuiti di pagamento nazionali e internazionali:
* PagoBANCOMAT / BANCOMAT Pay
* Carte Visa / Mastercard (Consumer, Commercial ed Extra)
* JCP (JCB)
* UPI (UnionPay International)

---

## 3. Flusso di Onboarding e Attivazione

Il processo di attivazione è progettato per ridurre il carico burocratico sul dealer.

1. **Raccolta Dati:** Il dealer compila il modulo di lead con i dati dell'esercente e l'IBAN di destinazione.
2. **Processo Acquiring:** Custom Pay e Nexi gestiscono le verifiche normative (KYC) e l'approvazione del contratto.
3. **Attivazione Dispositivo:** Una volta approvato, il terminale EDGE N+ riceve le credenziali di attivazione (Terminal ID) per l'abilitazione immediata dell'App SoftPOS.

[Presentazione soluzioni Custom Pay](assets/resources/TecnicoCpayFebbraio26.pptx)