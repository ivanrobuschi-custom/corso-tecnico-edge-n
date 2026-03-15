# IL TRIO PERFETTO PER LO SCAMBIO IMPORTO?
## **KEEPUP SMART + NEXI SOFTPOS + EDGE N+**

Il Custom EDGE-N+ rivoluziona l'operatività del punto vendita grazie alla sua architettura **"All-in-One"**. Essendo un dispositivo basato su **Android 13 GMS**, dotato di **antenna NFC** integrata e certificato per l'utilizzo delle tecnologie **SoftPOS (Tap to Pay)**, elimina completamente la necessità di interfacciarsi con un terminale POS bancario esterno!  
Questa grande dote di EDGE N+ è amplificata ancora di più grazie al software di vendita **KeepUp Smart**, pensato per supportare l'esercente in tutte le fasi di vendita e gestione del moderno punto cassa! 

L'integrazione nativa tra l'applicativo di cassa **KeepUp Smart** e la tecnologia **SoftPOS** (tramite convenzione Custom Pay) sul dispositivo **EDGE N+** rappresenta un'ottimizzazione architetturale per l'operatività del punto vendita, eliminando la necessità di interfacciamento con terminali bancari esterni.

## Vantaggi dell'Architettura Unificata

L'abilitazione dello scambio importo diretto all'interno del medesimo ecosistema hardware garantisce tre vantaggi tecnici fondamentali:

1. **Eliminazione degli Errori di Digitazione:** Il passaggio dell'importo dal carrello di KeepUp Smart all'applicativo bancario SoftPOS avviene tramite una chiamata di sistema nativa (Android Intent). Questo impedisce fisicamente all'operatore di digitare cifre errate sul POS, azzerando le squadrature di cassa a fine giornata tra l'emesso RT e il transato bancario.
2. **Riduzione dei Point of Failure (SPOF):** Non essendoci un collegamento fisico (cavo seriale/USB) o logico di rete (TCP/IP su LAN o Wi-Fi) tra la cassa e un POS esterno, si eliminano le latenze di comunicazione, i problemi di firewalling e le disconnessioni tipiche dei setup tradizionali.
3. **Semplificazione Diagnostica:** In caso di anomalia transazionale, il tecnico deve analizzare i log di un unico dispositivo Android, senza dover discriminare se il problema di comunicazione risiede nello switch di rete del cliente, nel cavo di collegamento o nell'hardware del terminale bancario.

---

## 🎬 VIDEO TUTORIAL PROCEDURA DI CONFIGURAZIONE SCAMBIO IMPORTO KUS/NEX SOFTPOS

<video controls width="100%">
  <source src="/corso-tecnico-edge-n/assets/resources/kussoft.mp4" type="video/mp4">
  Il tuo browser non supporta il tag video.
</video>

---

### Step 1: Configurazione del Terminale in KeepUp Smart

!!! warning "Prerequisiti di Sistema"
    Prima di procedere con il setup sull'applicativo, assicurarsi che:
    * Il dispositivo **EDGE N+** sia connesso a Internet.
    * L'App **SoftPOS Nexi/Custom Pay** sia installata, attivata con il Terminal ID (TID) dell'esercente e funzionante.
    * L'antenna NFC del dispositivo sia abilitata nelle impostazioni di Android.

1. Avviare l'applicativo **KeepUp Smart**.
2. Accedere al **STRUMENTI** (è richiesto l'accesso con profilo Amministratore).
3. Navigare nella sezione dedicata alle periferiche esterne: **Impostazioni > SERVIZI > SCAMBIO IMPORTO**.
4. Dal menu a tendina **"MODALITA' UTILIZZO POS"** selezionare l'opzione specifica per l'integrazione app-to-app: **SoftPOS**.
5. Abilitare flag **Scambio importo su dispositivo PoS**
6. Abilitare o meno **Stampa ricevuta esercente** e opzioni per stampa **Ricevuta cliente**.
6. **Salvare** la configurazione. 
    * *Nota Tecnica:* A differenza dei POS tradizionali, non sono richiesti parametri di indirizzamento IP o porte seriali, in quanto il payload viene scambiato internamente dal sistema operativo.

!!! note "Nota Bene"
    All'interno del software KeepUp Smart sono disponibili tasti funzione per effettuare facilmente:
    * Storno ultima operazione Pos eseguita
    * Ristampa ultima transazione
    * Chiusura POS
    * Richiesta di pagamento manuale senza documento commerciale

