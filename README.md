[readme.md](https://github.com/user-attachments/files/28568266/readme.md)
# BIO-SCANNER PRO - Sistema Vettoriale V5 🧬

**BIO-SCANNER PRO (V5 MEDICALCORE)** è un'applicazione web avanzata per l'analisi biomeccanica e posturale in tempo reale. Sviluppato per supportare professionisti del settore, il sistema utilizza la computer vision per tracciare i landmark articolari del corpo umano, calcolare i vettori anatomici e rilevare deviazioni posturali rispetto a target preimpostati.

---

## 🚀 Caratteristiche Principali

* **Tracciamento Vettoriale in Tempo Reale:** Utilizza la webcam per mappare il corpo umano a 33 punti (landmark) garantendo un'analisi fluida a 60fps.
* **Analisi Assiale (Testa / Tronco / Bacino):**
    * Misurazione del tilt orizzontale (Spalle e Anche).
    * Calcolo della deviazione dell'asse del tronco (linea bacino-spalle) rispetto alla verticale (0-45°).
    * Calcolo della deviazione dell'asse del collo (linea spalle-centro testa) rispetto alla verticale (0-90°).
* **Analisi Arti Superiori e Inferiori (0-180°):**
    * Impostazione di target angolari per i segmenti Spalla-Gomito, Gomito-Polso, Anca-Ginocchio e Ginocchio-Caviglia.
    * Calcolo dello scostamento angolare rispetto al vettore del tronco.
* **Tolleranze Personalizzabili e Feedback Visivo:** Gli slider permettono di impostare margini di tolleranza. Il sistema colora lo scheletro in tempo reale (Verde = OK, Giallo = Attenzione, Rosso = Critico).
* **Acquisizione Immagini Intelligente:**
    * Scatto manuale.
    * **Auto-Scatto in Fase Critica:** Cattura automaticamente un'istantanea quando il paziente entra in una zona "rossa" (con cooldown di 3 secondi per evitare scatti multipli accidentali).
* **Reportistica PDF Avanzata:** Generazione automatica di un referto in formato PDF contenente:
    * I valori posturali istantanei.
    * Una tabella comparativa (Sinistra vs Destra) con il calcolo dell'asimmetria (Delta Δ).
    * La galleria delle acquisizioni con i dati metrici specifici registrati al momento di ogni scatto.

---

## 🛠️ Tecnologie Utilizzate

L'applicazione è interamente client-side (non richiede server backend o database) e garantisce la massima privacy del paziente elaborando il feed video localmente sul dispositivo.

* **HTML5 / JavaScript (ES6)**: Struttura e logica del motore vettoriale.
* **Tailwind CSS**: Framework per un'interfaccia utente moderna, responsiva e in stile "medical-tech".
* **MediaPipe Pose (by Google)**: Modello di Machine Learning ottimizzato per il tracking posturale ad alta fedeltà.
* **jsPDF & jsPDF-AutoTable**: Librerie per la generazione, l'impaginazione e il download del referto medico in formato PDF.

---

## 📋 Guida all'Uso

### 1. Avvio del Sistema
1. Aprire il file `index.html` utilizzando un browser moderno (si consiglia Google Chrome o Microsoft Edge).
2. Cliccare sul pulsante **"▶ AVVIA SISTEMA"** posizionato al centro dello schermo visivo.
3. Autorizzare il browser all'utilizzo della webcam.

### 2. Impostazione dei Parametri
Sulla barra laterale destra sono presenti i moduli di controllo:
* **Modulo 1 (Assetto Assiale):** Imposta i limiti di attenzione (giallo) e criticità (rosso) per i dislivelli e per le deviazioni degli assi centrali.
* **Moduli 2 e 3 (Arti):** Definisci i target ideali (es. 0° per braccia perfettamente lungo i fianchi) e le tolleranze di errore accettabili.

### 3. Fase di Analisi e Reportistica (Modulo 4)
* Usa **"Scatta Foto Manuale"** per registrare la postura corrente.
* Attiva **"Auto-Scatto in Fase Critica"** durante gli esercizi dinamici: il sistema scatterà da solo quando rileva un errore fuori tolleranza.
* Concluso il test, clicca su **"Genera Report PDF"**. Il file verrà scaricato automaticamente sul computer contenente la tabella degli scostamenti angolari e le immagini acquisite.

---

## ⚠️ Disclaimer Medico

*BIO-SCANNER PRO è uno strumento di supporto visivo e di calcolo vettoriale. Non sostituisce il giudizio clinico di un medico, di un fisioterapista o di uno specialista della riabilitazione, né sostituisce esami diagnostici strumentali (es. radiografie). L'accuratezza dei vettori dipende dalla qualità della webcam, dall'illuminazione ambientale e dall'abbigliamento del soggetto (si consigliano indumenti aderenti).*
