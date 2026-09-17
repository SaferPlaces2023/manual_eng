# 🌧️ Safer\_RAIN

&#x20;

{% hint style="info" %}
**Il modello Safer\_RAIN è il modello di SaferPlaces per simulare scenari di allagamento di tipo Pluviale**
{% endhint %}

**Il modello Safer\_RAIN**  è un algoritmo gerarchico basato su DEM “_Filling-&-Spilling”_.&#x20;



Il modello poggia sulle seguenti principali assunzioni semplificative:

●        Gli effetti dinamici sono trascurati (cioè, l'algoritmo non risolve le equazioni dell'idrodinamica, ma si limita a valutare l'estensione dell'evento alluvionale e il livello dell'acqua nelle depressioni) e il volume d'acqua delle precipitazioni scorre a valle istantaneamente,

●        L' acqua scorre secondo il metodo D8 (si veda, ad esempio, O'Callaghan e Mark, 1984) \[1].

Maggiori dettagli sul modello Safer\_RAIN, sulla validazione e sul benchmarking sono disponibili nei documenti pubblicati da Samela et al. \[2] e Persiano et al. \[3] nel 2020, nonché da Essenfelder et al. \[4] e Mediero et al. \[5, 6] nel 2022 (vedi Bibliografia).

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption><p>Rappresentazione schematica del metodo Filling-&#x26;-Spilling: <br>(a) depressioni di primo livello, <br>(b) struttura gerarchica annidata delle depressioni in condizioni di pieno riempimento; <br>i pannelli (c) e (d) illustrano la rappresentazione ad albero dei contorni delle depressioni composite della zona umida, rispettivamente a sinistra e a destra. <br>Le diverse porzioni della depressione composita sono rappresentate con colori diversi: blu chiaro (primo livello), blu scuro (secondo livello), verde (terzo livello). Questa figura è tratta da Wu e Lane (2017) [7].</p></figcaption></figure>

L'algoritmo gerarchico “_Filling-&-Spilling”_ richiede i seguenti dati di input: &#x20;

1. un modello digitale di elevazione (DEM), necessario nella fase di preelaborazione per l'identificazione delle depressioni del terreno (chiamate "blue spot" in italiano “macchie blu”),
2. il volume soglia (espresso in metri cubi, ad esempio 100 m3) necessario per l'identificazione delle depressioni (o blue spots),
3. altezza della fetta di volume (solitamente dell'ordine di 0,01 m) necessaria nella fase di preelaborazione per identificare la morfologia di ciascuna depressione con il metodo del “level-set” (livello di impostazione); una fetta più sottile è associata a una migliore rappresentazione della morfologia delle macchie blu, ma richiede necessariamente tempi di calcolo più elevati,
4. profondità di pioggia associata all'evento di allagamento pluviale che deve essere riprodotto; questa informazione è necessaria per la fase di allagamento,
5. tasso di infiltrazione naturale e del sistema di drenaggio, necessario per calcolare l'entità dell'inondazione netta da pioggia.



<details>

<summary>Bibliografia modello Safer RAIN</summary>

Un elenco aggiornato delle pubblicazioni relative alla validazione ed applicazione dei modelli di SaferPlaces è disponibile al seguente [link](https://saferplaces.co/scientifically-proven-hazard-and-damage-modelling/)

</details>
