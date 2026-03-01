# FEATURES EDGE N

Il dispositivo **Custom EDGE N** è un Registratore Telematico Nativo basato su architettura PC POS Android.
Rappresenta la versione standard della famiglia EDGE, progettata per garantire stabilità nelle operazioni di cassa retail e nella gestione della mobilità (omologa ambulante).
A differenza del modello N+, la versione **EDGE N** utilizza un'architettura hardware dimensionata per l'esecuzione del punto cassa essenziale e la trasmissione telematica dei corrispettivi.

[EDGE_N]

---

## Architettura
Il sistema adotta un'architettura ibrida che unifica fisicamente ma separa logicamente il mondo gestionale da quello fiscale, garantendo stabilità e compliance normativa.

* **Modulo Applicativo (Android):** Gestisce l'interfaccia utente, la logica di vendita (App di cassa) e la connettività verso l'esterno. Agisce come "Master" del sistema.
* **Modulo Fiscale (RT):** Una board dedicata, dotata di processore sicuro (100 MHz) e memoria fiscale, che gestisce esclusivamente la firma dei corrispettivi, il DGFE e la comunicazione con l'Agenzia delle Entrate.
* **Bus di Comunicazione:** I due moduli comunicano internamente tramite una porta seriale virtualizzata. Questo è fondamentale per il troubleshooting: se l'App non vede la stampante, spesso è indice di un blocco su questo canale interno.

---

## Core System
La mainboard della versione EDGE N è progettata per ottimizzare i consumi energetici, ideale per l'uso a batteria, pur mantenendo le prestazioni necessarie per il software di cassa nativo.

| Componente | Specifica Tecnica EDGE N | Note Operative per Assistenza |
| :--- | :--- | :--- |
| **OS** | Android™ 12 | Versione standard ottimizzata per Retail. |
| **CPU** | Quad-Core 2.0 GHz | Processore bilanciato per garantire autonomia operativa in mobilità. |
| **RAM** | 2 GB | DDR3. *Nota:* Evitare l'esecuzione di app pesanti in background non necessarie alla vendita. |
| **Flash** | 32 GB eMMC | Spazio condiviso. Monitorare periodicamente l'occupazione della memoria se si archiviano molti log o backup. |
| **Sicurezza** | Processore Fiscale Dedicato | Garantisce l'integrità dei dati fiscali e la gestione della crittografia XML. |

---

## Interfacce e Connettività (I/O)
Il pannello posteriore, protetto dallo sportello *Cable Management*, ospita le connessioni fisiche. È essenziale mappare correttamente le porte durante l'installazione per evitare conflitti.

### Pannello Posteriore e Laterale
* **1x Ethernet (RJ45):** 10/100 Mbps. *Canale prioritario consigliato per la trasmissione telematica XML in postazione fissa.*
* **1x Seriale (RJ11):** RS232 standard. Utilizzabile per collegare display esterni legacy o PC in modalità stampante fiscale.
* **1x Cash Drawer (RJ12):** Supporta 12V/24V (Tipicamente 24V, verificare impostazioni).
* **1x USB Type-C:** Riservata esclusivamente per attività di **Service/Debug (ADB)**.
* **4x USB 2.0 Type-A:** Distribuite tra vano posteriore e accesso esterno (per scanner, tastiere o Pen Drive per export XML/aggiornamenti).

### Moduli Wireless
* **Wi-Fi:** Integrato (Supporto standard 2.4GHz / 5GHz).
* **Data Mobile:** 4G/LTE integrato (Slot Nano-SIM). *Essenziale per l'invio corrispettivi in mobilità.*
* **Bluetooth:** Integrato (Per scanner BT o pairing accessori).
* **NFC:** Integrato (Standard).

[descrizione]

---

## Sottosistema di Stampa
Il gruppo di stampa termico è identico meccanicamente su tutta la gamma, garantendo intercambiabilità dei consumabili.

* **Formato:** 57mm (Larghezza) x 50mm (Diametro rotolo).
* **Velocità:** 120 mm/sec.
* **Head Life:** 150 Km (Dato medio stimato).
* **Sensori:** Fine carta ottico riflessivo.
    * *Troubleshooting:* Se il dispositivo segnala "Fine Carta" ma il rotolo è presente, pulire il sensore ottico con aria compressa o un panno morbido asciutto.

---

## Alimentazione e Gestione Energetica

Il dispositivo EDGE N+ supporta un sistema di alimentazione ibrido che ne garantisce la piena operatività sia per installazioni Retail fisse che per scenari di mobilità avanzata, assicurando la continuità del servizio (fiscale e transazionale) anche in assenza di rete elettrica.

### Specifiche Tecniche Alimentazione
L'alimentazione primaria avviene tramite adattatore AC/DC esterno. È fondamentale utilizzare esclusivamente l'alimentatore fornito in dotazione per evitare instabilità che potrebbero compromettere i cicli di scrittura sulla memoria eMMC.

* **Input:** 100-240V ~ 50/60Hz.
* **Output:** 12V DC / 1A.
* **Connettore:** Jack DC standard (Polo positivo centrale).

### Modulo Batteria
Il dispositivo integra una batteria ricaricabile ad alta capacità, accessibile tramite vano dedicato sul fondo dello chassis.

* **Tecnologia:** Ioni di Litio (Li-Ion).
* **Specifiche:** 7.6V - 3000 mAh.
* **Autonomia:** L'autonomia effettiva varia in base al carico CPU (es. utilizzo intensivo app terze parti) e alla luminosità del display 8".

!!! warning "Procedura Critica: Prima Accensione"
    I dispositivi vengono spediti con una **linguetta isolante** applicata sui contatti della batteria per preservarne la carica durante lo stoccaggio.
    
    1.  **Prima di collegare l'alimentatore alla rete elettrica**, aprire il vano batteria.
    2.  Rimuovere fisicamente la linguetta isolante trasparente.
    3.  Richiudere il vano assicurandosi che il coperchio sia bloccato.
    
    **Nota di assistenza:** Se la linguetta non viene rimossa, il dispositivo si spegnerà immediatamente in caso di disconnessione accidentale dell'alimentatore, con rischio di corruzione dei dati in scrittura.

### Logica di Ricarica e Manutenzione
Il sistema di ricarica è gestito dal kernel Android.

1.  **Stato di Carica:** Monitorabile dall'icona batteria nella barra di stato superiore.
2.  **Ciclo di Vita:** Le prestazioni degradano dopo circa 300-500 cicli di ricarica completi.
3.  **Best Practice:** Anche se utilizzato in postazione fissa, si consiglia di effettuare cicli di scarica/carica periodici per mantenere calibrata la lettura della percentuale residua da parte del sistema operativo.


[EDGE_N]: assets/images/CUSTOM_Edge2.png
[descrizione]: assets/images/descrizionedisp.png