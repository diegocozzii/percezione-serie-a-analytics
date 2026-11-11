# Modern Serie A Analytics (1993 – 2026)
### Progetto per l'esame di Principi e Modelli della Percezione

**Gruppo di lavoro:**
- Diego Cozzi (51299A) 
- Mario Rovagnati (50644A) 
- Matteo Dini (51073A) 

---

## Obiettivo del progetto
Analisi quantitativa e visiva dell'evoluzione della Serie A negli ultimi 30 anni (**11.726 partite**) integrata con metriche avanzate di **Expected Goals (xG)** sul decennio 2014–2024 per le 10 squadre costantemente presenti nella massima divisione ($N=380$ partite ciascuna).

---

## Struttura del repository
- `data/`: Dataset consolidati e matrici aggregate:
  - `serie_a_partite.csv` (archivio storico completo 1993–2026)
  - `dati_slide7_tiri.csv`, `dati_slide8_classifica_storica.csv`, `dati_slide9_forbice.csv`
  - `dati_gol_reali_10_squadre.csv`, `dati_scostamento_gol_xg.csv`
- `notebooks/`: 
  - `analisi_serie_a_completo.ipynb` (pipeline riproducibile di estrazione, pulizia e generazione asset)
- `plots/`: Grafici esportati ad alta risoluzione (250 DPI) in duplice versione (*con guida metodologica* e versione *clean* muta per l'impaginazione nelle slide):
  - `g1_gol` (trend storico e picco 2020/21)
  - `g2_fattore_campo` (chiusura della forbice casa/trasferta)
  - `g_slide7_tiri` (volume tiri totali vs nello specchio dal 2005)
  - `g_slide8_punti` (ranking storico cumulativo standardizzato a 3 punti per vittoria)
  - `g_slide9_forbice` (gap punti tra vetta e salvezza)
  - `g_slide10_quadrante` (mappa tattica xG fatti vs xG subiti medi)
  - `g3_small_multiples` e `g3_heatmap_gol` (produzione offensiva per club a confronto di canali visivi)
  - `g4_heatmap_scostamento` e `g5_dumbbell_totale` (bilancio cinici vs spreconi: gol fatti vs gol attesi)
  - `g_slide12_caso_studio` (scostamento classifica reale vs punti attesi xPTS stagione 2017/18)

---

## Domande di ricerca e percorso narrativo (16 Slide)
1. **Come è cambiata la Serie A in 30 anni?** (Volume gol, crollo del fattore campo, evoluzione dello stile di tiro).
2. **Chi domina il campionato?** (Classifica storica trentennale, forbice scudetto-salvezza, profili offensivi decennali).
3. **Chi vince davvero: merito o fortuna?** (Analisi di cinismo realizzativo e scostamento tra gol effettivi e Expected Goals).

---

## Come riprodurre l'analisi
1. Aprire il notebook `notebooks/analisi_serie_a_completo.ipynb` su Google Colab.
2. Selezionare **Runtime → Esegui tutto**: la pipeline elabora l'archivio remoto, calcola le metriche, genera tutti i grafici ed esporta automaticamente.
