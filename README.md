# Impatto della Struttura del Capitale sulla Redditività delle Imprese ICT negli USA

Questo progetto di ricerca analizza la relazione tra la struttura del capitale e le performance di redditività delle aziende tecnologiche americane. Lo studio è ispirato alla ricerca di **Kim, Jung e Kim (2023)** sulle imprese ICT in Corea del Sud.

## 1. Obiettivo della Ricerca
L'obiettivo è determinare come fattori quali la leva finanziaria e la liquidità influenzino il valore e la redditività aziendale (misurata tramite ROE e ROA) nel contesto statunitense, controllando per variabili come dimensione ed età aziendale.

## 2. Metodologia
A differenza dello studio originale che utilizza un singolo anno e modelli DEA/Tobit, questo progetto adotta un approccio semplificato e robusto:
- **Campione**: Aziende quotate USA nei settori Software e Hardware.
- **Arco Temporale**: Media dei dati 2020-2024 per eliminare distorsioni annuali.
- **Modello Statistico**: Regressione Lineare Multipla (OLS) con errori standard robusti HC3.
- **Variabili**:
  - **Dipendente (Y)**: Redditività (ROE o ROA).
  - **Indipendenti (X)**: Debt-to-Equity Ratio (Leva), Current Ratio (Liquidità).
  - **Controllo**: Logaritmo del Totale Attivo (Dimensione) e log(1+Età) aziendale.
  - **Settoriale**: Dummy `software` (1 = Software, 0 = Hardware) e interazioni `software × regressori` per il modello ROA.
- **Controlli diagnostici e di robustezza**: VIF, Breusch-Pagan, Cook's distance, test di Chow robusto (Wald HC3), ristima sul campione filtrato con criterio IQR.

## 3. Struttura del progetto
- `01_Data_Cleaning.ipynb` — pulizia e preparazione dei dataset (winsorizzazione e versione IQR per robustezza)
- `02_Statistica_Descrittiva.ipynb` — statistiche descrittive, distribuzioni, matrice di correlazione, confronto Software/Hardware
- `03_Regressione_OLS.ipynb` — regressioni principali ROE e ROA, diagnostiche (VIF, BP, Cook), test di Chow robusto
- `04_Robustezza.ipynb` — ristima sui dati IQR e sensibilità a Cook's distance

## 4. Requisiti Tecnici
L'analisi è realizzata in Python utilizzando le seguenti librerie:
- `pandas`: Manipolazione e pulizia dei dati (gestione valori n.d./n.s.).
- `statsmodels`: Esecuzione dei modelli econometrici e test di significatività.
- `seaborn`/`matplotlib`: Visualizzazione dei dati e analisi dei residui.

## 5. Riferimento Scientifico
Kim, Y., Jung, S., & Kim, C. (2023). *The Impact of Capital Structure on the Profitability Performance of ICT Firms*. Processes, 11(2), 635. [https://doi.org/10.3390/pr11020635].
