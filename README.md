# Data Interoperability and Semantics – Practical Work 2  
##02 – Open Data Portals  

**Author:** JOUINI Saief Eddine  

---

## 1. Presentation of the Open Data Portal

In this work, I used the French open data portal **data.gouv.fr**.  
This portal is the official platform for open data in France. It is managed by **Etalab** and allows public administrations, local authorities, and private actors to publish open datasets.

**Data.gouv.fr provides:**
- Open access to datasets  
- Metadata describing each dataset  
- Downloadable files in machine-readable formats (CSV, JSON)  
- APIs for programmatic access  

Moreover, the portal promotes data standardization by encouraging or enforcing the use of official schemas, such as the **IRVE schema** for electric vehicle charging stations.

---

## 2. Type of Data Studied

The analysis focuses on **electric vehicle charging stations (IRVE)**.  
This type of data is particularly interesting because:
- It is regulated at the national level  
- Many different actors publish data (state, local authorities, private operators)  
- A national schema exists to harmonize the datasets  

The goal is to understand:
- Which metadata, formats, and schemas are recommended  
- Which ones are enforced  
- Which ones are actually used in practice  

---

## 3. List of the Datasets Used

The analysis is based on **10 datasets** published on *data.gouv.fr*:
1) Base nationale des IRVE (Infrastructures de Recharge pour Véhicules Électriques)

https://www.data.gouv.fr/datasets/base-nationale-des-irve-infrastructures-de-recharge-pour-vehicules-electriques

2) Infrastructures de recharge pour véhicules électriques (IRVE) — Communauté d’Agglomération du Pays de Grasse (réseau Wiiiz)

https://www.data.gouv.fr/datasets/infrastructures-de-recharge-pour-vehicules-electriques-irve-1/

3) Bornes de recharges CPS (IRVE) — IZIVIA

https://www.data.gouv.fr/datasets/bornes-de-recharges-cps/

4) Bornes de recharges IZIVIA Grand Lyon

https://www.data.gouv.fr/datasets/bornes-de-recharges-izivia-grand-lyon

5) Indigo-Open-Data-IRVE — Indigo Group

https://www.data.gouv.fr/datasets/indigo-open-data-irve

6) Infrastructure de Recharge Véhicules électriques (IRVE) — e-Totem Infrastructures

https://www.data.gouv.fr/datasets/infrastructure-de-recharge-vehicules-electriques-irve-e-totem-infrastructures

7) Bornes de Recharge IRVE du réseau R3 — groupe DBT

https://www.data.gouv.fr/datasets/bornes-de-recharge-irve-du-reseau-r3-groupe-dbt

8) Fichier IRVE Gireve

https://www.data.gouv.fr/datasets/fichier-irve-gireve

9) Bornes de recharge IRVE du réseau VIRTA

https://www.data.gouv.fr/datasets/bornes-de-recharge-irve-du-reseau-virta

10) Bornes de recharge publiques du réseau jerecharge.com

https://www.data.gouv.fr/datasets/bornes-de-recharge-publiques-du-reseau-jerecharge-com/

## 4. Synthetic Summary of Each Dataset

### 1. Base nationale des IRVE (France – consolidated dataset)

This dataset is the official national reference for electric vehicle charging stations in France.  
It is produced by **data.gouv.fr** and consolidates all local and private datasets that correctly follow the IRVE schema.

First, the metadata are very complete: the description is detailed, the licence is clearly defined, and the update frequency is daily.  
Then, the data format (CSV + API) is fully machine-readable and easy to reuse.  
Finally, the IRVE schema is strictly enforced, which guarantees a high level of consistency.

As a result, this dataset represents the best example of standardized and reusable open data on the portal.

---

### 2. IRVE – Pays de Grasse (Wiiiz)

This dataset is published by a local authority and focuses on charging stations in a specific territory.  
At first glance, the dataset follows the IRVE topic and provides useful local information.

However, metadata are incomplete: documentation is missing and the update frequency is not specified.  
Moreover, the dataset is flagged as not fully compliant with the IRVE schema, which prevents its integration into the national consolidated database.

Therefore, even if the data are useful at a local level, reuse at a national scale is limited.

---

### 3. Bornes de recharge CPS – IZIVIA

This dataset is published by IZIVIA, a major private charging operator.  
Technically, the dataset respects the IRVE schema and uses standard fields.

Nevertheless, the licence is not specified, which creates uncertainty for legal reuse.  
In addition, several fields are typed as simple strings, reducing semantic precision.

In conclusion, the dataset is technically reusable, but its legal and governance aspects are weak.

---

### 4. Bornes de recharge IZIVIA Grand Lyon

This dataset focuses on the Lyon metropolitan area.  
It is well structured and clearly aligned with the IRVE schema.

On the positive side, identifiers, geographic coordinates, and technical characteristics are correctly defined.  
On the negative side, metadata remain limited, especially regarding documentation and update frequency.

Thus, the dataset is easy to reuse technically, but could be improved in terms of transparency.

---

### 5. Indigo Open Data IRVE

This dataset is published by Indigo Group at a national level.  
It is one of the best-quality operator datasets in this analysis.

Indeed, the dataset strictly follows the IRVE schema and explicitly mentions the schema version used.  
In addition, the licence (ODbL) is clearly stated, and the update frequency is regular.

As a result, this dataset shows that private operators can produce high-quality and well-governed open data.

---

### 6. IRVE e-Totem Infrastructures

This dataset is produced by e-Totem Infrastructures, a national operator.  
From a technical point of view, the dataset is compliant with the IRVE schema and contains all key fields.

However, metadata quality is weak: the licence is not specified, documentation is missing, and the update frequency is not respected.  
This creates uncertainty for long-term reuse.

Therefore, the dataset is technically correct but poorly managed from an open data perspective.

---

### 7. Bornes de recharge IRVE du réseau R3 (groupe DBT)

This dataset is published by R3 (DBT Group), an industrial actor.  
It respects the IRVE schema and uses correct data types (boolean, date, integer).

Nevertheless, the description is very short and no documentation is provided.  
The licence is defined as “Other (Open)”, which is vague and not fully standard.

Consequently, the dataset is technically usable but lacks clarity and openness.

---

### 8. Fichier IRVE Gireve – Données statiques

This dataset plays a central role in the IRVE ecosystem.  
It is produced by Gireve, an interoperability platform that aggregates data from many operators.

The data are collected automatically via the OCPI protocol and converted to the IRVE schema.  
Metadata are very detailed, and the licence is clearly defined.

Thanks to its aggregation role and strong standardization, this dataset is highly reusable and reliable at a national scale.

---

### 9. Bornes de recharge IRVE du réseau VIRTA

This dataset is published by an individual contributor and is relatively old.  
It provides basic information about charging stations but does not follow the IRVE schema.

Field names are non-standard, some data types are incorrect, and encoding issues are visible.  
As a result, the dataset cannot be integrated into the national IRVE system.

This dataset illustrates the limits of non-standard and poorly governed open data.

---

### 10. Bornes de recharge publiques du réseau jerecharge.com

This dataset is published by jerecharge.com, a private operator.  
Technically, the dataset is well structured and compliant with the IRVE schema.

Identifiers are clean, geographic data are correct, and field types are well defined.  
However, the licence is missing and the update frequency is not respected.

In summary, the dataset is easy to use technically, but its legal reliability is limited.

# Final Synthesis: Recommended, Enforced and Used Practices on data.gouv.fr (IRVE datasets)

This analysis focuses on electric vehicle charging station data (IRVE) published on the French open data portal **data.gouv.fr**.  
Based on ten different datasets, it is possible to clearly distinguish what is **recommended**, **enforced**, and **actually used in practice** regarding metadata, formats, and schemas.

---

## 1. Metadata

### Recommended metadata

The portal recommends providing rich and clear metadata.  
In particular, datasets should include:
- A clear title  
- A detailed description explaining the context and the content  
- The name of the producer  
- A licence allowing reuse  
- Information about update frequency  

These elements help users understand the dataset without opening the file and improve trust and reuse.

### Enforced metadata

Some metadata elements are effectively enforced:
- A dataset must be linked to a producer  
- A licence must be declared to allow legal reuse  
- Basic metadata fields are required by the portal  

Without these elements, reuse becomes difficult or legally uncertain.

### Metadata used in practice

In practice, metadata quality is very heterogeneous.  
National institutions and aggregators (such as the base nationale IRVE or Gireve) provide complete and well-documented metadata.  
On the contrary, several private operators and individual contributors publish datasets with missing documentation, unclear update frequency, or unspecified licences.

As a result, metadata recommendations are not always followed.

---

## 2. Data Formats

### Recommended formats

Data.gouv.fr strongly recommends machine-readable formats, especially:
- CSV for tabular data  
- APIs for programmatic access  

These formats are simple, widely supported, and easy to process.

### Enforced formats

Although no single format is strictly mandatory, datasets intended for reuse and consolidation must be:
- Downloadable  
- Structured  
- Readable by machines  

In practice, CSV is the *de facto* enforced format for IRVE data.

### Formats used in practice

All analyzed datasets provide data in CSV format, often accompanied by an automatically generated API.  
This shows a strong convergence toward simple and reusable formats.

Therefore, format recommendations are well applied in practice.

---

## 3. Data Schemas

### Recommended schemas

For IRVE data, the use of the official **IRVE schema** is clearly recommended.  
This schema defines:
- Standardized field names  
- Data types  
- Identifiers  
- Geographic representations  

It aims to harmonize datasets from different producers.

### Enforced schemas

For datasets that must be integrated into the national consolidated IRVE database, the schema is strictly enforced.  
Only datasets compliant with the IRVE schema can be automatically consolidated.  
Non-compliant datasets remain isolated on the portal.

### Schemas used in practice

Most recent datasets published by professional actors follow the IRVE schema.  
However, older datasets or individual initiatives sometimes ignore it completely.

This shows that schema enforcement is effective at the national level, but weaker for independent publications.

---

## 4. Overall Conclusion

In conclusion, **data.gouv.fr** provides a strong framework for open data standardization.  
Formats and schemas are well defined and technically enforced for consolidation purposes.

However, the quality of metadata and governance still depends heavily on the producer.  
While institutional and professional actors generally follow best practices, others publish datasets with limited documentation and unclear reuse conditions.

Thus, the portal successfully encourages standardization, but full compliance remains uneven in practice.

