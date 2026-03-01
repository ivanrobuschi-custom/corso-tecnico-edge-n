# EDGE N+ Hardware e Architettura di Sistema

## Panoramica Architetturale

Il dispositivo Custom EDGE N+ è una soluzione All-in-One che integra in un unico chassis un PC POS Android e un Registratore Telematico Nativo. L'architettura è progettata per operare in mobilità (omologa ambulante) o in postazione fissa.

A differenza del modello precedente, la versione N+ si basa su una piattaforma hardware potenziata per supportare applicazioni di vendita complesse (es. Keep Up Smart) e pagamenti digitali (SoftPOS) senza latenze.

Scheda Tecnica: Core System
La mainboard gestisce il sistema operativo e la logica applicativa, separata logicamente dal modulo fiscale ma integrata fisicamente.

| Componente | Specifica Tecnica EDGE N+ | Note Operative |
| :--- | :--- | :--- |
| OS | Android™ 13 | Supporto GMS (Google Mobile Services) e OTA. |
| CPU | Hexa-Core (2x Cortex-A78 + 4x Cortex-A55) | Architettura big.LITTLE per efficienza energetica. |
| RAM | 4 GB | DDR4, necessaria per gestione multitasking fluido. |
| Flash | 64 GB | eMMC. Spazio disponibile per App di terze parti e DB locali. |
| Sicurezza | Modulo Fiscale Hardware + Tamper Elettronico | Vedi sezione 1.4 per dettagli sul Sigillo. |

[def]: https://