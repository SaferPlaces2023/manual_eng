---
hidden: true
cover: ../.gitbook/assets/Asset 10.jpg
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: hero
    mask: none
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# 💰 Misure di mitigazione Edifici del danno

Additional mitigation measures are available that directly target damage reduction at various scales (across an entire area or for a single building). Users can assign different damage reduction measures to multiple buildings, such as wet or dry floodproofing, flood barriers, adaptive use of the ground floor, vertical evacuation, building elevation, and activity relocation. Table 1 summarizes all these measures.

In SaferPlaces, these measures can be considered by reducing the simulated water depth that may cause damage, raising defenses, or reducing the value of the exposed assets once they are transferred or moved above the flood level.

&#x20;

Table 1 – Flood Mitigation

<table data-header-hidden><thead><tr><th width="156">Misura</th><th>Descrizione</th><th width="144">Effetto sulle perdite</th><th>Applicabilità</th></tr></thead><tbody><tr><td>Impermeabilizzazione secca degli edifici</td><td>Una barriera che protegge l'intero edificio dall'inondazione fino a una determinata altezza</td><td><p>Nessuna perdita per l'edificio o il contenuto se la profondità dell'acqua è inferiore all'altezza della barriera       </p><p> </p></td><td>Tutti gli edifici</td></tr><tr><td>Impermeabilizzazione umida dell'edificio</td><td>L'impermeabilizzazione di porte, finestre, scantinati, ecc. protegge l'interno dell'edificio dall'inondazione fino a una determinata altezza.</td><td>Nessuna perdita per il contenuto se la profondità dell'acqua è inferiore all'altezza dell'impermeabilizzazione.</td><td>Tutti gli edifici</td></tr><tr><td>Uso adattato del piano terra</td><td>Spostare al piano superiore i grandi elettrodomestici, gli utensili e i beni durevoli per la ricreazione*.</td><td>Nessuna perdita per gli oggetti non conservati al piano terra, se la profondità dell'acqua è inferiore al primo piano***.</td><td>Edifici monofamiliari di almeno 2 piani</td></tr><tr><td>Evacuazione verticale delle attività</td><td>Evacuazione di beni durevoli di piccole dimensioni (elettronica, medicinali, cura della persona ed effetti personali) al piano superiore**</td><td>Nessuna perdita subita dagli oggetti evacuati se la profondità dell'acqua è inferiore al primo piano***.</td><td>Tutti gli edifici di almeno 2 piani</td></tr><tr><td>Innalzamento del piano terra</td><td>L'elevazione del piano terra viene aumentata di una determinata altezza.</td><td>Profondità dell'acqua ridotta di una determinata altezza durante l'esecuzione del modello di vulnerabilità BN</td><td>Tutti gli edifici</td></tr><tr><td>Trasferimento di beni</td><td>L'edificio viene demolito e ricostruito in un luogo più sicuro.</td><td>Nessuna perdita per l'edificio o il contenuto</td><td>Tutti gli edifici</td></tr></tbody></table>

[\* COICOP elementi 5.3, 5.5 and 9.2. \*\* COICOP elementi 6.1, 8.2, 9.1, 12.1 and 12.3. \*\*\* Il valore della riduzione delle perdite dipende dalla composizione stimata del contenuto della casa per area pilota, mentre l'altezza del primo piano è fissata a 3,3 m dal suolo.](#user-content-fn-1)[^1]

{% hint style="info" %}
The "_Mitigations_" tool ( [top-bar.md](../saferplaces-gui-web/top-bar.md "mention")) is specific to each building: with a right-click on any building, users can modify the function used for damage calculation and add specific mitigation measures for that building.
{% endhint %}

The "Damage Preview" tool displays a panel with the prediction of damages in terms of Expected Annual Damage (EAD) calculated for different return periods (2, 5, 10, 50, 100 years), baseline scenarios (from ERA5 Land and Copernicus/NASA data), and climate scenarios (SSP4.5 and 8.5) from global climate projections CMIP6, projected to 2050 or 2100. An example is illustrated in the

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption><p>Pannello di previsione dei danni, ottenuto con lo strumento “<em>Damage Preview</em>”.</p></figcaption></figure>



[^1]: 
