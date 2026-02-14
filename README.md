# Modelli di memoria di lavoro basati su reti neurali spiking eterogenee con plasticità sinaptica a breve termine

Questo repository contiene la tesi di laurea triennale in Fisica (A.A. 2023/2024), discussa presso l'Università degli Studi di Cagliari.

**Autore:** Simone Rubiu  
**Relatore:** Prof. Bruno Golosio  
**Co-relatore:** Dott. Gianmarco Tiddia  

## Descrizione del Progetto

Il lavoro di tesi si inserisce nel campo delle **neuroscienze computazionali** e si concentra sullo studio della **memoria di lavoro** (working memory), il processo cognitivo deputato all'immagazzinamento temporaneo e all'elaborazione delle informazioni.

L'obiettivo principale è analizzare i limiti e la robustezza del modello computazionale di *working memory* basato sulla **plasticità sinaptica a breve termine (STP)**, originariamente proposto da Mongillo et al. (2008). In particolare, lo studio introduce elementi di **eterogeneità** (variabilità parametrica) all'interno della rete neurale per renderla biologicamente più realistica e verificarne la stabilità.

### Concetti Chiave
* **Spiking Neural Networks (SNN):** Utilizzo del modello neuronale *Leaky Integrate-and-Fire* (LIF).
* **Short-Term Plasticity (STP):** Implementazione di meccanismi di facilitazione (STF) e depressione (STD) sinaptica per il mantenimento dell'informazione.
* **Eterogeneità:** Introduzione di distribuzioni di probabilità (gaussiane/uniformi) per parametri chiave come pesi sinaptici e costanti temporali, superando l'approccio classico a parametri costanti.

## Strumenti e Metodologia

Le simulazioni presentate nella tesi sono state realizzate utilizzando:
* **NEST Simulator:** Per la simulazione della dinamica delle reti neurali spiking.
* **Python:** Per l'analisi dati e la generazione dei grafici (Raster plots, istogrammi dei ratei di fuoco).

## Struttura della Tesi

Il documento `Tesi_Triennale_Simone_Rubiu.pdf` è suddiviso nei seguenti capitoli:

1.  **Il Sistema Nervoso:** Introduzione biologica ai neuroni, membrane e sinapsi.
2.  **La Modellizzazione:** Descrizione matematica del neurone LIF e del modello di plasticità a breve termine (modello di Tsodyks-Markram).
3.  **La Memoria di Lavoro:** Panoramica sui modelli psicologici (Baddeley) e computazionali (Hopfield, reti spiking).
4.  **Modello di Working Memory:** Dettagli sull'implementazione della rete spiking, protocolli di simulazione e meccanismi di *Population Spikes*.
5.  **Analisi dei Risultati:** Studio dell'impatto dell'eterogeneità su:
    * Pesi sinaptici potenziati ($J_p$) e di base ($J_b$).
    * Valori iniziali delle variabili sinaptiche ($u, x$).
    * Costanti temporali di facilitazione ($\tau_f$) e depressione ($\tau_d$).
    * Frazione di sinapsi facilitate vs non facilitate.

## Risultati Principali

Lo studio ha dimostrato che:
* La rete neurale mostra una notevole **robustezza**: nonostante l'introduzione di eterogeneità nei parametri chiave, il modello continua a sostenere l'attività di memoria di lavoro.
* La variabilità delle **costanti temporali** ($\tau_f, \tau_d$) e la **frazione di sinapsi facilitate** sono i fattori che influenzano maggiormente la dinamica della rete.
* È necessaria una frazione minima di circa l'**80-90% di sinapsi facilitate** per mantenere attivo il meccanismo di memoria durante il periodo di attesa (delay period).

## Riferimenti

Per maggiori dettagli sul modello originale o sul simulatore utilizzato:
* *Mongillo et al., Science (2008)* - Synaptic theory of working memory.
* *NEST Simulator* - [nest-simulator.org](https://www.nest-simulator.org/)

---
*Repository a scopo di archiviazione accademica.*
