# DISMISSIONE RT

## Normativa Dismissione

Dal punto di vista normativo, secondo le Specifiche Tecniche RT dell'Agenzia delle Entrate, la "Dismissione" rappresenta la fase conclusiva e irreversibile del ciclo di vita di un Registratore Telematico.
Tale stato comporta la cessazione definitiva di ogni operatività fiscale e logica del dispositivo, rendendolo permanentemente inidoneo alla memorizzazione e trasmissione dei corrispettivi.

Questa procedura è normativamente richiesta in casistiche definitive, quali lo **SMALTIMENTO** dell'hardware, un guasto tecnico irreparabile, l'**MEMORIA DI RIEPILOGO ESAURITA**.
A differenza della Disattivazione, al termine del processo di Dismissione il Registratore Telematico non può in alcun modo essere riattivato o ricollocato presso alcun esercente.

!!! warning "NOTA BENE"
    È fondamentale comprendere l'irreversibilità di questa variazione di stato. Una volta che il Registratore Telematico viene posto in stato di "Dismesso", il certificato del dispositivo viene revocato definitivamente dall'Agenzia delle Entrate.
    Analogamente alla disattivazione, la dismissione deve essere comandata fisicamente dall'hardware per garantire il corretto allineamento con il cassetto fiscale dell'esercente e prevenire anomalie o scarti sul portale "Fatture e Corrispettivi".

## Procedura di Dismissione tramite UtilityX RT

- Aprire l'app **UtilityX RT**, selezionare la voce **MENÙ TECNICO** e inserire la password di protezione 147896.
- Selezionare la voce **EVENTO**.
- Accedere al pannello di gestione degli stati della macchina e selezionare **DISMISSIONE**.
- Selezionare la causale o il Codice Evento appropriato per la dismissione:
    - 601 - ALTRO: _Se viene selezionata questa voce, diventa obbligatorio compilare anche il campo "Descrizione" inserendo il motivo tecnico specifico della dismissione._
    - 606 - SMALTIMENTO
    - 609 - MEMORIA DI RIEPILOGO ESAURITA
    
- Premere il tasto **REGISTRA EVENTO**

_**Esito**_: Il registratore telematico genererà un file con estensione .xml (contenente l'ultimo invio dei corrispettivi e la comunicazione di variazione stato in "Dismesso") che verrà trasmesso in automatico al sistema dell'Agenzia delle Entrate.
_**Stampa di Controllo**_: A conferma del successo dell'operazione, la stampante emetterà un documento non fiscale con l'attestazione di avvenuta dismissione.

!!! wanrning "ATTENZIONE"
    Da questo momento il Registratore Telematico è DISMESSO in modo permanente. Non sarà più possibile emettere documenti commerciali né ripristinare la macchina per utilizzi fiscali futuri.