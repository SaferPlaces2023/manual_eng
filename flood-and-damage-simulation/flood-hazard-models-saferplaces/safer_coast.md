# 🏖️ Safer\_COAST

{% hint style="info" %}
&#x20;**Safer\_COAST è dedicato alla modellazione del rischio di inondazione costiera**
{% endhint %}

Si tratta di un modello basato su DEM 0D, molto più semplice delle rappresentazioni idrodinamiche 2D, ottenuto promuovendo la semplificazione dei processi fisici che descrivono il processo di inondazione costiera e rimuovendo la discretizzazione temporale nel processo di calcolo.

Safer\_COAST non utilizza modelli fisici idraulici, ma mira a mappare l'estensione dell'inondazione attraverso la diffusione del livello dell'acqua utilizzando la gravità e il DEM come input principali.

Safer\_COAST considera la connettività idrologica, ad esempio il passaggio dell'acqua da una cella all'altra, e richiede che, oltre a trovarsi al di sotto del livello di inondazione, un'area sia collegata idrologicamente alla fonte dell'inondazione (ad esempio, l'oceano o il fiume) per essere inondata.

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption><p>Differenza tra gli approcci basati su DEM 0D <br>a) regola di connettività zero che mostra che tutte le celle del raster con quota &#x3C;= 1 sono allagate; <br>b) regola di connettività idrologica D-4 per 1 m di <em>Storm Surge Level</em> (livello di mareggiata) in cui la cella è allagata solo se è connessa al corpo del mare direttamente o tramite celle adiacenti in direzioni cardinali; <br>c) regola di connettività idrologica D-8 per 1 m di <em>Storm Surge Level</em> in cui la cella è allagata solo se è connessa al corpo del mare direttamente o tramite celle adiacenti in direzioni cardinali o diagonali.</p></figcaption></figure>

Di solito si ottiene inondando tutti i pixel raster della pianura alluvionale che rispettano le seguenti regole topologiche e fisiche:

1. il pixel è collegato alla fonte di inondazione (fiume o costa),&#x20;
2. l'altezza del pixel è superiore all'altezza dell'acqua di inondazione,
3. il volume dell'inondazione è sufficiente per allagare il pixel (bilancio idrico).

Le principali assunzioni del modello di alluvione costiera a crescita regionale Safer\_COAST sono:

1. volume d'acqua infinito
2. i risultati rappresentano la massima estensione teorica dell'inondazione dopo un tempo infinito e senza tener conto del sovrascorrimento,
3. l'acqua scorre da una cella all'altra (metodo D8).

I modelli 0D basati su DEM che sono stati progettati per una rapida analisi e caratterizzazione degli eventi di piena, richiedono solo due input principali, ovvero:

1. Modello digitale di elevazione: Specifica i valori costanti per la fase e il momento x e y al confine.
2. Livelli dell'acqua - Livelli di sovratensione: Come un confine di Dirichlet, ma con un comportamento che varia nel tempo.



