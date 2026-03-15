# Aggiornamento Normativo: Variazioni Specifiche Tecniche RT (4 Marzo 2026)

Il 4 marzo 2026 l'Agenzia delle Entrate ha pubblicato un aggiornamento relativo alle specifiche tecniche per i corrispettivi telematici, sancendo il passaggio ufficiale dal documento "Specifiche tecniche RT V11.1" alla nuova versione V11.2.

!!! note "Nota bene"
    
    La serie **EDGE** ad oggi marzo 2026 è omologata alla versione V11.1, come da disposizioni di legge. Presenta a bordo ultimo fw 15.03.75 il quale recepisce la normativa relativa alla gestione del [_Sigillo Fiscale Digitale._](tamper.md)

## 1. Gestione Opzionale dei Buoni Pasto
Viene introdotta una nuova modalità opzionale per l'elaborazione, la registrazione e l'esposizione dei buoni pasto all'interno delle transazioni.  

*Azione Tecnica*: Verificare l'allineamento del firmware RT e la configurazione del frontend di cassa (es. KeepUp Smart) per assicurare che il flusso XML recepisca la nuova gestione fiscale o figurativa dei ticket restaurant, garantendo la corretta totalizzazione nei corrispettivi giornalieri.

## 2. Modifica Strutturale dei Documenti Gestionali
Per inibire qualsiasi potenziale confusione con i documenti commerciali fiscalmente rilevanti, la normativa impone modifiche ferree al layout di stampa delle transazioni non fiscali (preconti, proforma, riepiloghi tavoli).  

*Azione Tecnica*: Adeguamento dei layout di stampa interni. È obbligatoria l'introduzione di elementi grafici e marcatori visivi che identifichino inequivocabilmente la non validità ai fini fiscali del documento cartaceo emesso dalla stampante dell'RT.

## 3. Sigillo Fiscale Digitale (Requisiti Minimi)
La direttiva definisce formalmente i requisiti minimi architetturali per l'implementazione e l'utilizzo del Sigillo Fiscale Digitale.  

*Azione Tecnica*: Valutazione della conformità delle procedure di sicurezza. Questa specifica si innesta sui sistemi di protezione hardware (tamper elettronico) già implementati sui dispositivi EDGE, standardizzando i protocolli di validazione crittografica per l'integrità del dispositivo.
Vai direttamente alla pagina: [_Sigillo Fiscale Digitale._](tamper.md)

## 4. Aggiornamento Tracciati DGFE e Memoria Fiscale
Viene effettuata la sostituzione integrale degli allegati strutturali per l'esportazione delle memorie di massa.  

*Azione Tecnica*: Il precedente Allegato - Tracciato DGFE e memoria fiscale (V3.1) viene deprecato in favore della versione V3.2. Le procedure di estrazione dati su MicroSD o tramite tool di diagnostica (UtilityX RT) devono essere conformi al nuovo XML schema per garantire la validità dei file esportati durante le ispezioni.

## 5. Nuovi Ambiti di Utilizzo dei Dispositivi RT
La normativa estende i campi di applicazione dei Registratori Telematici introducendo due nuovi ambiti di utilizzo specifici.  

*Azione Tecnica*: Parametrizzazione in fase di messa in servizio (Censimento/Attivazione) per mappare correttamente il dispositivo sul portale Fatture e Corrispettivi, a seconda del nuovo settore operativo in cui viene installato.
