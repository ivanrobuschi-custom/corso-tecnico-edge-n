# NUOVA GESTIONE CHIUSURE GIORNALIERE

### OBBLIGO CHIUSURA FISCALE ENTRO LE ORE 24:00

Il registratore telematico deve eseguire, una **chiusura giornaliera entro le ore 24 del giorno di apertura.**
Nel caso in cui l’operatore del registratore telematico non esegua la chiusura giornaliera entro le ore 24.00 del giorno di apertura, il registratore telematico **_blocca l’emissione di documenti commerciali_** e richiede una chiusura giornaliera. 

#### Avviso di Chiusura fiscale obbligatoria
Per avvisare l’esercente dell’imminente richiesta di chiusura giornaliera, il registratore telematico EDGE ad ogni scontrino emesso successivamento **alle ore 23:30** avvisa l'operatore con apposito WARNING visualizzato a display e con segnalazione acustica di effettuare un azzeramento di chiusura giornaliera.

< **NOTA BENE**
Nel caso in cui l'operatore, superate le ore 23:30 effettui un azzeramento, come richiesto con WARNING, ma successivamente emetta, entro le ore 23.58, anche un solo documento commerciale, sarà necessaria una ulteriore chiusura giornaliera, giornata di nuovo aperta >

#### Blocco scontrinazione ore 23:58
Se entro le ore 23:58 non è stata eseguita la chiusura di giornata tramite azzeramento, il registratore telematico serie EDGE entra in stato di **BLOCCO**, Il registratore emette un documento gestionale con un messaggio bloccantee inibisce tutte le operazioni di vendita.
L'unica operazione consentita è l'azzeramento fiscale.

< Un eventuale documento commerciale iniziato prima della mezzanotte viene stornato automaticamente ed integralmente se non terminato entro la mezzanotte. In questa situazione sul documento viene riportato come motivo dello storno la frase “STORNO PER CHIUSURA FORZATA”, prima del totale complessivo. >

In caso di interruzione/spegnimento/dimenticanza dell’esecuzione della chiusura giornaliera il registratore telematico, alla sua prima riaccensione, potrà **esclusivamente** come sola operazione la chiusura della giornata lasciata precedentemente aperta o non eseguita, inserendo come giorno di rilevazione nel tag <DataOraRilevazione> secondo quanto previsto dal tracciato record [Tipi Dati per i Corrispettivi ver 7.1](assets/resources/AllegatoTipiDatiperiCorrispettiviver7.1.pdf) la data e l’ora della giornata non chiusa, come memorizzato sulla memoria permanente di dettaglio.
