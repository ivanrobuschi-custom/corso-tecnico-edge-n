# Normativa e Gestione del Periodo di Inattività (RT V11.1)

In base alle specifiche tecniche per i Registratori Telematici (versione 11.1), la normativa prevede regole precise per la gestione dei periodi in cui il punto vendita non opera e, di conseguenza, non effettua trasmissioni. Il comportamento atteso dal dispositivo varia in funzione della durata dell'inattività dell'esercente.

## Interruzioni di attività fino a 12 giorni

Nelle casistiche di interruzione dell’attività dovuta a chiusura settimanale, chiusura domenicale, ferie brevi, eventi eccezionali o attività stagionale (e non causata da malfunzionamenti tecnici), non è richiesta un'azione preventiva da parte dell'esercente. 

Il Registratore Telematico gestisce autonomamente il buco temporale: alla prima trasmissione successiva alla riapertura, o all’ultima trasmissione utile, il dispositivo elabora e invia un unico file[cite: 2010]. Tale file conterrà la totalità dei dati relativi al periodo di interruzione ad importo zero, andando a coprire tutti i giorni per i quali non è stata effettuata l’operazione di chiusura giornaliera.

## Interruzioni superiori a 12 giorni o di durata ignota

La procedura cambia se l’interruzione dell’attività è superiore ai 12 giorni (ad esempio per ferie lunghe, chiusura stagionale o inutilizzo temporaneo), oppure qualora l’esercente non sia in grado di conoscere a priori la durata esatta del periodo di inattività. 

In questi scenari, il Registratore Telematico serie EDGE ha la possibilità di comunicare tempestivamente al sistema dell'Agenzia delle Entrate l’inizio del periodo di inutilizzo, inviando un evento di tipo “fuori servizio” caratterizzato dal codice di dettaglio "608" (Magazzino/Periodo di inattività).

Alla ripresa lavorativa, non è necessaria alcuna procedura di riattivazione manuale da parte del tecnico o dell'esercente: il Registratore Telematico tornerà automaticamente nello stato “In servizio” nel momento in cui effettuerà la prima trasmissione utile[cite: 2012].

## Procedura Operativa su Dispositivi Custom EDGE (Firmware V11)

Per agevolare l'esercente nell'adempimento normativo relativo alle inattività prolungate o ignote, sui dispositivi Edge è stata implementata una funzione rapida a livello di firmware.

È possibile mandare la cassa in stato di "Fuori Servizio per Periodo Inattivo" utilizzando un apposito shortcut: 
* L'operatore deve semplicemente digitare il **CODICE 1600** confermando con il tasto **Chiave**. Questo comando forza l'invio dell'evento con codice 608 al server dell'Agenzia delle Entrate.  
Oppure tramite utilizzo di applicativo UtilityX rt 
* Selezionare _MENU' TECNICO_
* 147896
* Evento
* FUORI SERVIZIO
* Codice 608 - magazzino
* Registra Evento

Vedi video tutorial [Fuori Servizio](assets\resources/fuoriservizio.mp4)