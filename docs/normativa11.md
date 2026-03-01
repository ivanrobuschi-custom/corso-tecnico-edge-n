# NORMATIVA XML 7 versione 11.1

## Nuova Gestione delle Chiusure Giornaliere

- Obbligo entro le 24:00: Il Registratore Telematico deve eseguire la chiusura giornaliera entro la mezzanotte.
- Blocco Operativo: Se la chiusura non viene effettuata, il RT blocca l'emissione di nuovi documenti commerciali e forza la chiusura.
- Gestione Server RT: I Server RT chiudono in automatico i punti cassa che non hanno inviato la disponibilità, trasmettendo appositi codici di anomalia all'Agenzia

## Gestione Inattività

- **Inattività Prolungata**: Se il periodo di chiusura supera i 12 giorni (o è di durata indefinita), il RT deve inviare obbligatoriamente un evento di "Fuori Servizio" con codice 608 (Magazzino/Inattività)

## Nuovi Servizi API: Messaggistica e Allineamento

- **Allineamento RT con server AdE**: Introdotto un servizio che obbliga il RT a riallinearsi con i sistemi dell'Agenzia dell' Entrate in caso di discordanza (evidenziata dall'errore 200), bloccando il dispositivo fino alla sincronizzazione.
- **Messaggistica Alert**: L'Agenzia può ora inviare messaggi codificati (alert bloccanti e non bloccanti, es. "Firmware non conforme") direttamente sul display e sulla stampa del RT@
- **Messaggistica Alert**: L'Agenzia può ora inviare messaggi codificati (alert bloccanti e non bloccanti, es. "Firmware non conforme") direttamente sul display e sulla stampa del RT

## Lotteria Istantanea e Documenti Digitali

- **Codice Bidimensionale**: Implementati i requisiti per stampare il codice bidimensionale necessario per la Lotteria ad estrazione istantanea, valido per pagamenti interamente elettronici
- **Scontrino Digitale Firmato**: I documenti commerciali digitali emessi tramite stampa virtuale devono ora essere firmati mediante il certificato del dispositivo (formati PADES o CADES)


