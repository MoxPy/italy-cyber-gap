# Indici di vulnerabilità strutturale: un'analisi statistica comparata tra Italia ed Europa sulla Cybersecurity

### Questa repository contiene il codice sorgente, i dataset e i Jupyter Notebook utilizzati per il progetto di tesi. 

La ricerca indaga un'anomalia statistica definita "Paradosso Italiano": la forte sproporzione tra il peso economico/demografico del Paese e l'elevata incidenza degli attacchi cyber subiti a livello globale. Attraverso l'analisi dei dati, il progetto quantifica questa esposizione e dimostra la correlazione diretta tra la vulnerabilità del sistema Italia e la carenza strutturale di specialisti ICT nel tessuto imprenditoriale, confrontata con la media dell'Unione Europea.

## Struttura della Repository
L'analisi segue i capitoli della tesi ed è divisa per step logici:

* `data/raw/`: File CSV originali estratti dai report.
* `data/processed/`: Dati puliti e uniti, pronti per l'analisi statistica.
* `notebooks/`: 
  * `02_analisi_italia.ipynb`: Trend e distribuzione degli incidenti in Italia per settore.
  * `03_confronto_europeo.ipynb`: Gap del capitale umano ICT.
  * `04_inferenza_statistica.ipynb`: Matrici di correlazione, test statistici e scatter plot.
* `reports/figures/`: Output grafici generati dal codice e inseriti nel documento di tesi.

## Stack Tecnologico
Tutto il workflow è stato sviluppato e testato su **JetBrains DataSpell**. 

Per garantire performance e riproducibilità sui dataset eterogenei, si è optato per il seguente stack:
* **Polars**: Per l'ingestione e la manipolazione dei dati.
* **NumPy & SciPy**: Utilizzati per le operazioni vettoriali e per i test di inferenza statistica del capitolo conclusivo.
* **Matplotlib & Seaborn**: Per la fase di Exploratory Data Analysis e la generazione dei grafici finali.

## Fonti Dati
I dati grezzi analizzati derivano dall'integrazione di database istituzionali e report di settore:
* **ACN** (Agenzia per la Cybersicurezza Nazionale)
* **Eurostat**
* **ISTAT** 
* **Clusit** (Rapporto sulla sicurezza ICT in Italia)
* **Check Point Research** (Global Threat Intelligence)

## Riproducibilità
Per eseguire i notebook in locale e riprodurre i grafici:

```bash
# Clona la repository
git clone https://github.com/MoxPy/italy-cyber-gap.git
cd tesi-manuel

# Installa le dipendenze richieste
pip install -r requirements.txt