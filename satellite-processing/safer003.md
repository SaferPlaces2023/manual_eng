---
description: Mappe di intensità delle precipitazioni
---

# 🛠️ Safer003

The "Safer003" function consists of custom algorithms to generate a precipitation intensity map from satellite data. The output of Safer003 is used as input to improve flood risk mapping caused by pluvial floods.

The opening panel requires the user to input three parameters as requested by the Safer003 module:

\- _from date_: data dell'evento di alluvione,

\- _lag (days)_: n° di giorni consecutivi all'evento, in cui il sistema deve verificare la disponibilità dei dati,

\- _step:_ intervallo temporale richiesto.

The workflow for ingesting rainfall data relies on the use of PERSIANN-PDIR NOW [http://chrsdata.eng.uci.edu/](http://chrsdata.eng.uci.edu/).

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>Mappe di intensità delle precipitazioni</p></figcaption></figure>



