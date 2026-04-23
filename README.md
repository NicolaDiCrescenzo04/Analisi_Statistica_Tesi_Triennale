# Impatto della Struttura del Capitale sulla Redditività delle Imprese ICT negli USA

Questo progetto di ricerca analizza la relazione tra la struttura del capitale e le performance di redditività delle aziende tecnologiche americane. Lo studio è ispirato alla ricerca di **Kim, Jung e Kim (2023)** sulle imprese ICT in Corea del Sud.

## 1. Obiettivo della Ricerca
L'obiettivo è determinare come fattori quali la leva finanziaria e la liquidità influenzino il valore e la redditività aziendale (misurata tramite ROE e ROA) nel contesto statunitense, controllando per variabili come dimensione ed età aziendale.

## 2. Metodologia
A differenza dello studio originale che utilizza un singolo anno e modelli DEA/Tobit, questo progetto adotta un approccio semplificato e robusto:
- **Campione**: Aziende quotate USA nei settori Software e Hardware.
- **Arco Temporale**: Media dei dati 2021-2025 per eliminare distorsioni annuali.
- **Modello Statistico**: Regressione Lineare Multipla (OLS).
- **Variabili**:
  - **Dipendente (Y)**: Redditività (ROE o ROA).
  - **Indipendenti (X)**: Debt-to-Equity Ratio (Leva), Current Ratio (Liquidità).
  - **Controllo**: Logaritmo del Totale Attivo (Dimensione) e Anni di attività (Età).

## 3. Requisiti Tecnici
L'analisi è realizzata in Python utilizzando le seguenti librerie:
- `pandas`: Manipolazione e pulizia dei dati (gestione valori n.d./n.s.).
- `statsmodels`: Esecuzione dei modelli econometrici e test di significatività.
- `seaborn`/`matplotlib`: Visualizzazione dei dati e analisi dei residui.

## 4. Riferimento Scientifico
Kim, Y., Jung, S., & Kim, C. (2023). *The Impact of Capital Structure on the Profitability Performance of ICT Firms*. Processes, 11(2), 635. [https://doi.org/10.3390/pr11020635].
