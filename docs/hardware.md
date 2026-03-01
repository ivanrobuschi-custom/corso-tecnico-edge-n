# EDGE N+

Il dispositivo **Custom EDGE N+** è una soluzione All-in-One che integra in un unico chassis un *PC POS Android e un Registratore Telematico Nativo*.
L'architettura è progettata per operare in mobilità (omologa ambulante) o in postazione fissa.
A differenza del modello Edge N, la versione **EDGE N+** si basa su una piattaforma hardware potenziata per supportare applicazioni di vendita complesse (es. KeepUp Smart) e pagamenti digitali (SoftPOS) senza latenze.

![EDGE N+]

---

## Architettura
Il sistema adotta un'architettura ibrida che unifica fisicamente ma separa logicamente il mondo gestionale da quello fiscale, garantendo stabilità e compliance normativa.

* **Modulo Applicativo (Android):** Gestisce l'interfaccia utente, la logica di vendita (App di cassa), la connettività verso l'esterno e i pagamenti digitali (NFC). Agisce come "Master" del sistema.
* **Modulo Fiscale (RT):** Una board dedicata, dotata di processore sicuro e memoria fiscale, che gestisce esclusivamente la firma dei corrispettivi, il DGFE e la comunicazione con l'Agenzia delle Entrate.
* **Bus di Comunicazione:** I due moduli comunicano internamente tramite una porta seriale virtualizzata ad alta velocità. Questo è fondamentale per il troubleshooting: se l'App non vede la stampante, spesso è indice di un blocco su questo canale interno.

---

## Core System
La mainboard della versione N+ è dimensionata per gestire carichi di lavoro intensivi, come l'esecuzione simultanea del software di cassa e dei servizi in background per i pagamenti elettronici (SoftPOS).

| Componente | Specifica Tecnica EDGE N+ | Note Operative per Assistenza |
| :--- | :--- | :--- |
| **OS** | Android™ 13 | Versione con supporto GMS (Google Mobile Services). Supporta aggiornamenti OTA. |
| **CPU** | Hexa-Core (2x Cortex-A78 + 4x Cortex-A55) | Architettura big.LITTLE: i core A78 gestiscono i picchi (es. pagamenti), gli A55 mantengono il sistema efficiente. |
| **RAM** | 4 GB DDR4 | Fondamentale per evitare il kill delle App in background durante l'uso intensivo. |
| **Flash** | 64 GB eMMC | Lo spazio è partizionato. Verificare sempre lo spazio disponibile prima di scaricare log o backup database massivi. |
| **Sicurezza** | Crypto-chip Hardware | Gestisce le chiavi crittografiche per la firma XML e la sicurezza dei pagamenti Tap-to-Phone. |

---

## Interfacce e Connettività (I/O)
Il pannello posteriore, protetto dallo sportello *Cable Management*, ospita le connessioni fisiche. È essenziale mappare correttamente le porte durante l'installazione per evitare conflitti.

### Pannello Posteriore
* **1x Ethernet (RJ45):** 10/100/1000 Mbps. *Canale prioritario consigliato per la trasmissione telematica XML.*
* **1x Seriale (RJ11):** RS232 standard. Utilizzabile per collegare display esterni legacy o bilance checkout.
* **1x Cash Drawer (RJ12):** Supporta 12V/24V (verificare selettore/impostazione software).
* **1x USB Type-C:** Riservata esclusivamente per attività di **Service/Debug (ADB)**. Non collegare periferiche di vendita qui.
* **2x USB 2.0 Type-A:** Per scanner barcode, tastiere o Pen Drive (aggiornamento FW/Loghi).

### Moduli Wireless
* **Wi-Fi:** Dual Band (2.4GHz / 5GHz) 802.11 ac.
* **Data Mobile:** 4G/LTE integrato (Slot Nano-SIM). *Essenziale per ambulanti.*
* **NFC:** Modulo avanzato sul fronte (cornice display) certificato per accettazione pagamenti Contactless (SoftPOS).

---

## Sottosistema di Stampa
Il gruppo di stampa termico è integrato nello chassis. La manutenzione preventiva è carico dell'esercente o del tecnico in visita periodica.

* **Formato:** 57mm (Larghezza) x 50mm (Diametro rotolo).
* **Velocità:** 120 mm/sec.
* **Head Life:** 150 Km (Dato medio stimato).
* **Sensori:** Fine carta ottico riflessivo.
    * *Troubleshooting:* Se il dispositivo segnala "Fine Carta" ma il rotolo è presente, pulire il sensore ottico con aria compressa o un panno morbido asciutto.

---

## Alimentazione e Sicurezza Tamper
Il dispositivo è dotato di protezioni hardware attive contro le manomissioni fiscali.

### Tamper Elettronico (Warning Critico)
A differenza dei registratori classici con piombo fiscale, EDGE N+ utilizza un **Sigillo Elettronico**.
* **Il Trigger:** Una vite specifica nel vano connessioni chiude un circuito di sicurezza.
* **L'Evento:** La rimozione della vite (anche a macchina spenta) scatena l'evento **TAMPER**.
* **Conseguenza:** Il dispositivo entra in blocco fiscale irreversibile ("Dispositivo Manomesso").
* **Ripristino:** Richiede procedura di **Inizializzazione Hardware (HW Init)** da parte di un laboratorio abilitato. **Non svitare mai senza procedura di servizio attiva.**

### Gestione Energetica
* **Input:** 12V DC / 1A.
* **Batteria:** Li-Ion 7.4V - 3000 mAh.
    * *Nota Installazione:* Alla prima accensione, è **obbligatorio** rimuovere la linguetta isolante nel vano batteria, altrimenti il dispositivo si spegnerà in caso di blackout o disconnessione rete elettrica.


[EDGE N+]: assets/images/EDGE-N+_5.png