# Modern Serie A Analytics (1993 – 2026)
### Progetto per l'esame di Principi e Modelli della Percezione

**Gruppo di lavoro:**
- Diego Cozzi (51299A) 
- Mario Rovagnati (50644A) 
- Matteo Dini (51073A) 

---

## Obiettivo del progetto
Analisi quantitativa e visuale dell'evoluzione della Serie A negli ultimi 30 anni (**11.726 partite**) integrata con metriche avanzate di **Expected Goals (xG)** sul decennio 2014–2024 per le 10 squadre costantemente presenti nella massima divisione ($N=380$ partite ciascuna).

---

## Struttura del repository
- `data/`: Dataset consolidati e matrici aggregate:
  - `serie_a_partite.csv` (archivio storico completo 1993–2026)
  - `dati_slide7_tiri.csv`, `dati_slide8_classifica_storica.csv`, `dati_slide9_forbice.csv`
  - `dati_gol_reali_10_squadre.csv`, `dati_scostamento_gol_xg.csv`
- `notebooks/`: 
  - `analisi_serie_a_definitivo.ipynb` (pipeline riproducibile di estrazione, pulizia e generazione asset)
- `plots/`: Grafici ad alta risoluzione (250 DPI) in duplice versione (*con guida metodologica* e versione *clean* per le slide):
  - `g1_gol` (trend storico e picco 2020/21)
  - `g2_fattore_campo` (chiusura della forbice casa/trasferta)
  - `g3_small_multiples` e `g3_heatmap_gol` (volumi realizzativi per club)
  - `g4_heatmap_scostamento` e `g5_dumbbell_totale` (confronto gol segnati vs occasioni create xG)

---

## Domande di ricerca e percorso narrativo (16 Slide)
1. **Come è cambiata la Serie A in 30 anni?** (Volume gol, crollo del fattore campo, evoluzione dei tiri).
2. **Chi domina il campionato?** (Classifica storica a 3 punti per vittoria, forbice scudetto-salvezza, profili offensivi decennali).
3. **Chi vince davvero: merito o fortuna?** (Analisi di efficacia e scostamento reale tra gol fatti e gol attesi).

---

## Come riprodurre l'analisi
1. Aprire il file `notebooks/analisi_serie_a_definitivo.ipynb` su Google Colab o Jupyter.
2. Eseguire l'intero blocco (**Runtime → Esegui tutto**): la pipeline scarica i dati remoti, calcola gli aggregati ed esporta tutti i grafici nella cartella locale.
