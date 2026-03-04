# DISALLINEAMENTI RT / PORTALE AGENZIA ENTRATE

La gestione dei disallineamenti tra il Registratore Telematico (RT) e il server dell'Agenzia delle Entrate (AE) è un fondamentale meccanismo di sicurezza e controllo introdotto nativamente con le Specifiche Tecniche RT V11.1.
Questo meccanismo serve a prevenire l'uso fraudolento o errato della cassa quando le informazioni presenti sul cassetto fiscale differiscono da quelle della macchina fisica. Ecco nel dettaglio come funziona, come viene rilevato e come si risolve:

### Cause di Disallineamento

Il problema nasce dal fatto che se un utente (esercente o commercialista) modifica lo stato del Registratore Telematico direttamente sul portale web "Fatture e Corrispettivi" dell'Agenzia delle Entrate (ad esempio passandolo da "In Servizio" a "Disattivato"), il dispositivo fisico locale non è in grado di allinearsi da solo con questa nuova informazione. Si crea così un'incongruenza tra lo stato reale della macchina (che crede di poter ancora lavorare) e lo stato telematico (che le vieta di farlo).

### Come il RT Rileva l'Incongruenza (Il Meccanismo)

Per ovviare a questa mancanza di comunicazione automatica, il RT è stato dotato di un apposito servizio SSL (chiamato dispositivi/allineamentodispositivo) che confronta lo stato locale con quello memorizzato sul server dell'Agenzia.
Il rilevamento (e il conseguente aggiornamento dello stato) scatta in momenti precisi:
* Dopo una Chiusura Giornaliera (Z): Se il RT invia la chiusura e riceve un esito negativo (come un errore http 409 / 200 XML), la macchina richiede immediatamente l'aggiornamento dello stato dal server per capire se è stata disattivata.
All'apertura di un documento commerciale: Il dispositivo verifica se lo stato sul server risulta "Disattivato" mentre la cassa è ancora attiva.
Dopo ogni segnalazione di evento: Il RT richiede l'aggiornamento dello stato del server dopo aver trasmesso un qualsiasi evento.
* Il Blocco Operativo: quando il RT si accorge del disallineamento critico (es. server "Disattivato" vs cassa "In servizio"), interviene un blocco di protezione severo:
Il Registratore Telematico non emette più documenti commerciali fino a quando il problema non viene risolto.
Per avvisare l'esercente, il RT visualizza un avviso a display e stampa un documento gestionale con la dicitura esatta: "ATTENZIONE! DISPOSITIVO BLOCCATO NECESSARIO INTERVENTO TECNICO PER LO SBLOCCO".

### L'Eccezione: Il "Fuori Servizio"
Le specifiche normative prevedono una deroga importante: il blocco del registratore telematico non si applica se il disallineamento riguarda lo stato "FUORI SERVIZIO". Se la macchina viene messa in fuori servizio dal portale, alla successiva trasmissione tornerà automaticamente "In Servizio" senza bloccarsi.

## La Risoluzione (Riallineamento)
Poiché il blocco è una misura di sicurezza antifrode, l'esercente non può sbloccare la cassa in autonomia.
È necessario l'intervento di un Tecnico Abilitato, il quale dovrà eseguire una nuova procedura di ATTIVAZIONE direttamente dal dispositivo per ripristinare il corretto stato sul server.
Una volta che il tecnico ha ripristinato lo stato corretto, alla successiva chiusura fiscale (Chiusura Z) andata a buon fine, la cassa si riallineerà definitivamente con il server dell'Agenzia delle Entrate, rimuovendo il blocco.

[**VEDI PROCEDURA DI RIALLINEAMENTO**](docs/errore409.md)