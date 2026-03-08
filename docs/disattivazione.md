# DISATTIVAZIONE RT

## Introduzione Normativa alla Disattivazione

Dal punto di vista normativo, secondo le Specifiche Tecniche RT V11.1 dell'Agenzia delle Entrate, la "Disattivazione" è una variazione di stato fondamentale per la corretta gestione del ciclo di vita di un Registratore Telematico.
Tale stato comporta la cancellazione formale dell'associazione logica tra la matricola del dispositivo e la Partita IVA dell'esercente uscente, provocando la contestuale sospensione del certificato del RT.

Questa procedura è normativamente richiesta e tracciata con specifici codici in casistiche precise, quali la cessione del dispositivo a terzi (a qualsiasi titolo, inclusa la vendita di macchine usate, rivenditori o trasformazioni societarie sostanziali) o in caso di furto.
Al termine del processo di disattivazione, il Registratore Telematico perde la sua operatività fiscale e diviene atto ad emettere esclusivamente Documenti Gestionali.

!!! warnin "NOTA BENE"
    È cruciale, come indicato dalle nuove regole sulla gestione dei disallineamenti, che questa variazione di stato venga comandata direttamente dal dispositivo fisico e trasmessa al server telematico.
    Se un esercente disattiva la cassa esclusivamente dal portale web "Fatture e Corrispettivi", si crea un'incongruenza critica che manda in blocco la macchina impedendo l'emissione di documenti commerciali. 
    [vedere risoluzione disallineamento](docs/errore409.md)
    Eseguendo la disattivazione in modo corretto dall'hardware, il dispositivo giustifica l'assenza di futuri invii telematici e permette al tecnico di effettuare successivamente la "ricollocazione", associando il RT alla Partita IVA di un eventuale nuovo esercente tramite una nuova attivazione.

## Procedura di Disattivazione tramite UtilityX RT

- Aprire l'app **UtilityX RT**, selezionare la voce **MENÙ TECNICO** e inserire la password di protezione 741236.
- Selezionare la voce **EVENTO**
- Accedere al pannello di gestione degli stati della macchina e selezionare **DISATTIVAZIONE**
- Selezionare Codice Evento:
    - 601 ALTRO: _Se viene selezionato il codice corrispondente ad "Altro", diventa obbligatorio compilare anche il campo "Descrizione" inserendo il motivo specifico della disattivazione_
    - 603 CESSIONE
    - 604 FURTO
- Premere il tasto **REGISTRA EVENTO**

_**Esito**_: Il registratore telematico creerà un file con estensione .xml (contenente i corrispettivi a zero e il codice dell'evento) che verrà inviato in automatico all'Agenzia delle Entrate.
_**Stampa di Controllo**_: A conferma del successo dell'operazione, la stampante emetterà un documento non fiscale con la dicitura: "PROCEDURA DI DISATTIVAZIONE COMPLETATA!

!!! warning 
    da questo momento la RT è disattivata e non sarà possibile emettere DOCUMENTI COMMERCIALI!

