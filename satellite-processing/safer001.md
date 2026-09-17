---
description: >-
  Automatic extraction of the mask related to the extension of the fled areas in
  post-event condition.
---

# 🛠️ Safer001

Activating the tool "Satellite" from the top bar initiates the function, called Safer001, which allows the user to automatically generate the flood area mask within the activated calculation domain.

The flooded area will refer to a specific temporal event lasting a few days and will be produced by analyzing both SAR and Optical images from Copernicus Sentinel and COSMO SKY MED.

The opening panel requires the user to input the four parameters needed by the Safer001 module:

* _from date_: date of the flood event,
* _lag (days)_: number of consecutive days from the event during which the system must check data availability,
* _bbox_: bounding box or area of interest,
* _DEM_: the best available DEM will be passed to the Safer

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>Safer001 - Estrazione automatica della maschera di acqua alluvionale</p></figcaption></figure>



