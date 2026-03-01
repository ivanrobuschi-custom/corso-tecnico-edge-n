# EDGE N Hardware e Architettura di Sistema

## Panoramica Architetturale

Il dispositivo Custom EDGE N è un Registratore Telematico Nativo basato su architettura PC POS Android. Rappresenta la versione entry-level della famiglia EDGE, progettata per garantire stabilità nelle operazioni di cassa standard e nella gestione della fatturazione elettronica e telematica.

Il sistema unifica in un solo chassis la logica applicativa (Android) e la sicurezza fiscale (RT), mantenendo però una separazione logica tra i due ambienti per garantire l'integrità dei dati fiscali.

A differenza della serie N+, il modello EDGE N utilizza un'architettura hardware dimensionata per l'esecuzione del punto cassa essenziale.

| Componente | Specifica Tecnica EDGE N | Note Operative |
| :--- | :--- | :--- |
| OS | Android™ 12 | Versione standard per compatibilità applicativa Retail. |
| CPU | Quad-Core 2.0 GHz | Processore ottimizzato per consumi ridotti. |
| RAM | 2 GB | DDR3. Nota: Evitare il sovraccarico con app in background non necessarie. |
| Flash | 32 GB | eMMC. Spazio condiviso tra OS, DGFE e Applicativi. |
| Fiscale | Processore dedicato 100 MHz | Gestisce esclusivamente la crittografia e la memoria fiscale. |