# Introduzione di modelli markoviani e tecniche di apprendimento per l'analisi delle fratture pelviche
Analisi predittiva di 991 casi di frattura pelvica in emergenza. Il lavoro integra Machine Learning (LASSO) per identificare i predittori chiave (ISS, GCS, Hb) e modelli stocastici markoviani per simulare le traiettorie cliniche dei pazienti. Sviluppato in Python, il progetto offre un approccio data-driven al supporto decisionale in Pronto Soccorso

Autore: Mariastella Gioia La Rocca, Mia Rodotà
Università: Sapienza University of Rome
Relatore: Marco Isopi
Data: Luglio 2026

## Abstract
Lo studio analizza un campione di 991 pazienti traumatizzati utilizzando un approccio ibrido che combina il Machine Learning e la modellazione stocastica. Attraverso la tecnica di regolarizzazione LASSO, sono stati identificati i predittori clinici più significativi (ISS, GCS, Hb), mantenendo la massima interpretabilità medica. Questi parametri sono stati utilizzati per definire gli stati di una Catena di Markov, permettendo di simulare le traiettorie cliniche e calcolare le probabilità di transizione verso l'esito finale (sopravvivenza o decesso).

## Metodologia
Il lavoro è strutturato in quattro fasi principali:
1. **Data Cleaning & Profiling**: Gestione rigorosa dei dati mancanti e distinzione semantica del valore "zero" clinico. Rimozione degli outlier e standardizzazione Z-score dei parametri.
2. **Analisi Esplorativa (EDA)**: Studio bivariato delle distribuzioni (ISS, Lattati, Età) e analisi delle correlazioni di Spearman.
3. **Feature Selection (LASSO)**: Selezione dei predittori tramite metodo embedded (Penalizzazione L1) per ridurre la dimensionalità mantenendo l'identità fisica delle variabili.
4. **Modellazione Markoviana**: Costruzione di una Catena di Markov a tempo discreto con stati definiti dai cut-off clinici dei predittori selezionati.

## Struttura del Repository
*   `tesi_code.py`: Script Python principale per il pre-processing, la selezione LASSO e il calcolo delle matrici di transizione.
*   `requirements.txt`: Elenco delle librerie necessarie per l'esecuzione.
*   `/grafici`: Cartella contenente i grafici prodotti (Heatmap, Boxplot, Curve di Rischio).
*   `data_sample.csv`: (Esempio) Struttura dati richiesta per far girare il modello.

## Requisiti
Per eseguire il codice è necessario Python 3.9+ e le seguenti librerie:
*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `scikit-learn`

Puoi installare tutto tramite:
```bash
pip install -r requirements.txt
