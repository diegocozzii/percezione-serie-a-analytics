# Clustering degli Stili Tattici nella Serie A con K-Means e DBSCAN
### Progetto per l'esame di Principi e Modelli della Percezione

**Gruppo di lavoro:**
- Diego Cozzi (51299A)
- Mario Rovagnati (50644A)
- Matteo Dini (51073A)

---

## Obiettivo del progetto
Applicazione di algoritmi di apprendimento non supervisionato (**K-Means** e **DBSCAN**) ai dati della Serie A (dal 2005/06 al 2025/26) per raggruppare le coppie squadra-stagione in base allo stile di gioco (8 variabili tecniche medie a partita), tenendo fuori i punti in classifica per una validazione esterna finale e isolando le stagioni anomale come rumore.

---

## Struttura del repository
- `notebooks/analisi_serie_a_clustering_finale.ipynb`: pipeline riproducibile su Google Colab (download dati, creazione dataset squadra-stagione, EDA, normalizzazione con `StandardScaler`, gomito/silhouette, K-Means + PCA, DBSCAN ed esportazione ZIP).
- `data/`: dataset consolidati e assegnazioni finali dei cluster (`serie_a_partite_2005_2026.csv`, `dataset_squadra_stagione.csv`, `cluster_assegnazioni.csv`).
- `plots/`: grafici ad alta risoluzione in doppia versione (`_con_guida.png` e `_clean.png`).

---

## Come riprodurre l'analisi
1. Aprire `notebooks/analisi_serie_a_clustering_finale.ipynb` su Google Colab.
2. Selezionare **Runtime → Esegui tutto** per scaricare i dati, eseguire il clustering e generare l'archivio `progetto_serie_a_finale.zip`.
