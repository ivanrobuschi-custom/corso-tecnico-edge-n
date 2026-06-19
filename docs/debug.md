# Debug ADB su Edge N+: Wireless vs USB

Questa guida è rivolta alle **software house** e agli sviluppatori che necessitano di eseguire il debug della propria applicazione Android sull'**Edge N+** tramite Android Debug Bridge (ADB).

---

## Il problema: il debug USB non sempre funziona

L'**Edge N+** è un dispositivo Android 13 specializzato con modulo fiscale integrato. A differenza di uno smartphone consumer, la porta USB potrebbe avere comportamenti non standard o restrizioni che impediscono la corretta inizializzazione del canale ADB via cavo.

!!! warning "Attenzione"
    Il debug USB su alcuni modelli Edge richiede configurazioni particolari per funzionare correttamente. **La soluzione consigliata da Custom S.p.A. è il debug wireless (ADB over Wi-Fi/Ethernet)**, che risulta più stabile e affidabile.

---

## Prerequisito: abilitare le Opzioni Sviluppatore

Prima di qualsiasi operazione di debug, è necessario sbloccare le **Opzioni sviluppatore** sul dispositivo:

1. Vai su **Impostazioni → Info sul dispositivo → Informazioni sul software**
2. Individua la voce **Numero build**
3. Tocca **7 volte consecutive** sulla voce "Numero build"
4. Il sistema mostrerà il messaggio: *"Sei diventato uno sviluppatore"*
5. Torna in **Impostazioni**: comparirà la nuova voce **Opzioni sviluppatore**

---

## Scenario A — Debug Wireless (Wi-Fi) ✅ Consigliato

È la modalità **raccomandata** per Edge N+. Permette di lavorare senza cavi e funziona su qualsiasi rete locale.

### Sul dispositivo Edge N+

1. Vai su **Impostazioni → Opzioni sviluppatore**
2. Abilita **Debug USB** (necessario anche per il wireless)
3. Abilita **Debug wireless**
4. Il sistema mostrerà l'**indirizzo IP** del dispositivo e la **porta** (es. `192.168.1.50:5555`)

!!! tip "Suggerimento"
    L'indirizzo IP del dispositivo è visibile anche da **Impostazioni → Rete e Internet → Wi-Fi → [rete connessa] → dettagli**.

### Sul PC sviluppatore (stessa rete Wi-Fi)

Apri un terminale e lancia:

```bash
adb connect 192.168.1.50:5555
```

Verifica la connessione con:

```bash
adb devices
```

Output atteso:

```
List of devices attached
192.168.1.50:5555    device
```

A questo punto puoi eseguire il debug normalmente dal tuo IDE (Android Studio, VS Code, ecc.).

---

## Scenario B — Debug Wireless via Ethernet

Se il dispositivo Edge N+ è collegato alla rete tramite **cavo Ethernet** (es. in ambiente retail fisso), la procedura è identica: si usa comunque `adb connect` con l'indirizzo IP assegnato dalla rete LAN.

1. Recupera l'IP Ethernet da **Impostazioni → Rete e Internet → Ethernet**
2. Procedi come nello Scenario A dal punto "Sul PC sviluppatore"

```bash
adb connect 192.168.1.XX:5555
```

---

## Scenario C — Debug USB (se strettamente necessario)

Se per esigenze specifiche è necessario il debug via cavo USB:

1. Vai su **Impostazioni → Opzioni sviluppatore**
2. Abilita **Debug USB**
3. Collega il cavo USB (Type-C o USB maschio-maschio, a seconda del modello)
4. Sul dispositivo apparirà il popup: **"Consentire il debug USB?"** → tocca **OK**
5. Verifica sul PC:

```bash
adb devices
```

!!! warning "Nota importante"
    Su alcuni modelli Edge il debug USB potrebbe non essere rilevato correttamente dal PC, indipendentemente dal tipo di cavo utilizzato. In questo caso, **passa al debug wireless** (Scenario A).

---

## Riepilogo

| Modalità | Cavo necessario | Stabilità su Edge N+ | Note |
|---|---|---|---|
| **Wireless (Wi-Fi)** | No | ✅ Alta | Consigliata da Custom S.p.A. |
| **Wireless (Ethernet)** | Solo cavo di rete | ✅ Alta | Ideale per postazioni fisse |
| **USB** | Sì (Type-C / USB-A) | ⚠️ Variabile | Dipende dal modello; usare come ultima opzione |

---

## Comandi ADB utili

```bash
# Connetti al dispositivo
adb connect <ip>:5555

# Lista dispositivi connessi
adb devices

# Installa un APK
adb -s <ip>:5555 install app.apk

# Visualizza log in tempo reale
adb -s <ip>:5555 logcat

# Disconnetti
adb disconnect <ip>:5555
```

---
