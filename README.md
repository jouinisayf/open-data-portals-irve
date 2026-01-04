# Data Interoperability and Semantics – Practical Work 2  
## 02 – Open Data Portals  

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


## 2. Type of Data Studied

The analysis focuses on **electric vehicle charging stations (IRVE)**.  

The goal is to understand:
- Which metadata, formats, and schemas are recommended  
- Which ones are enforced  
- Which ones are actually used in practice  



## 3. Synthetic Summary of Each Dataset

The analysis is based on **10 datasets** published on *data.gouv.fr*

### 1. Base nationale des IRVE (France – consolidated dataset)  

https://www.data.gouv.fr/datasets/base-nationale-des-irve-infrastructures-de-recharge-pour-vehicules-electriques

This dataset is the official national reference for electric vehicle charging stations in France.  
It is published on **data.gouv.fr** and brings together all local and private datasets that correctly follow the IRVE schema.

The metadata are very complete: the description is clear, the licence is well defined, and the data are updated every day.  
The dataset is available in CSV format and through an API, which makes it easy to use.  
In addition, the IRVE schema is strictly applied, ensuring strong consistency between all records.

Overall, this dataset is a very good example of well-standardized and highly reusable open data.



### 2. IRVE – Pays de Grasse (Wiiiz)  

https://www.data.gouv.fr/datasets/infrastructures-de-recharge-pour-vehicules-electriques-irve-1/

This dataset is published by a local authority and describes charging stations in the Pays de Grasse area.  
It provides useful information for local users and follows the general IRVE topic.

However, some metadata are missing. There is no clear documentation, and the update frequency is not indicated.  
In addition, the dataset is marked as not fully compliant with the IRVE schema, so it cannot be included in the national database.

As a result, the dataset is useful at a local level, but difficult to reuse at a national scale.



### 3. Bornes de recharge CPS – IZIVIA  

https://www.data.gouv.fr/datasets/bornes-de-recharges-cps/

This dataset is published by IZIVIA, a major private operator of charging stations.  
From a technical point of view, the dataset follows the IRVE schema and uses standard field names.

However, the licence is not specified, which makes legal reuse unclear.  
Also, some fields are stored as simple text, even when more precise data types could be used.

In summary, the dataset is technically usable, but its legal and governance aspects are weak.



### 4. Bornes de recharge IZIVIA Grand Lyon  

https://www.data.gouv.fr/datasets/bornes-de-recharges-izivia-grand-lyon

This dataset focuses on charging stations in the Grand Lyon area.  
It is well structured and clearly aligned with the IRVE schema.

Identifiers, geographic coordinates, and technical information are correctly provided.  
However, metadata are limited, especially regarding documentation and update frequency.

Therefore, the dataset is easy to use from a technical perspective, but transparency could be improved.



### 5. Indigo Open Data IRVE  

https://www.data.gouv.fr/datasets/indigo-open-data-irve

This dataset is published by Indigo Group at a national level.  
It is one of the highest-quality datasets among those analyzed.

The IRVE schema is fully respected, and the schema version is clearly mentioned.  
The licence (ODbL) is well defined, and updates are made on a regular basis.

This dataset shows that private operators can publish open data that are both high-quality and well managed.



### 6. IRVE e-Totem Infrastructures  

https://www.data.gouv.fr/datasets/infrastructure-de-recharge-vehicules-electriques-irve-e-totem-infrastructures

This dataset is published by e-Totem Infrastructures, a national charging operator.  
Technically, it follows the IRVE schema and includes all the main required fields.

However, the quality of metadata is low. The licence is missing, documentation is not provided, and the update frequency is not respected.  
This creates uncertainty for long-term reuse.

As a result, the dataset is technically correct but poorly managed from an open data point of view.



### 7. Bornes de recharge IRVE du réseau R3 (groupe DBT)  

https://www.data.gouv.fr/datasets/bornes-de-recharge-irve-du-reseau-r3-groupe-dbt

This dataset is published by R3 (DBT Group), an industrial actor.  
It follows the IRVE schema and uses appropriate data types such as boolean, date, and integer.

However, the description is very short and no documentation is available.  
The licence is indicated as “Other (Open)”, which is vague and not fully standard.

Therefore, the dataset is technically usable but lacks clarity and openness.



### 8. Fichier IRVE Gireve – Données statiques  

https://www.data.gouv.fr/datasets/fichier-irve-gireve

This dataset plays an important role in the IRVE ecosystem.  
It is published by Gireve, an interoperability platform that collects data from many operators.

The data are gathered automatically using the OCPI protocol and then converted into the IRVE schema.  
Metadata are detailed, and the licence is clearly specified.

Thanks to its aggregation role and strong standardization, this dataset is highly reliable and reusable at a national level.



### 9. Bornes de recharge IRVE du réseau VIRTA  

https://www.data.gouv.fr/datasets/bornes-de-recharge-irve-du-reseau-virta

This dataset is published by an individual contributor and has not been updated recently.  
It provides basic information about charging stations but does not follow the IRVE schema.

Field names are not standardized, some data types are incorrect, and encoding problems are visible.  
Because of this, the dataset cannot be integrated into the national IRVE system.

This example shows the limitations of non-standard and poorly governed open data.



### 10. Bornes de recharge publiques du réseau jerecharge.com  

https://www.data.gouv.fr/datasets/bornes-de-recharge-publiques-du-reseau-jerecharge-com/

This dataset is published by jerecharge.com, a private operator.  
From a technical perspective, the dataset is well structured and compliant with the IRVE schema.

Identifiers and geographic data are correct, and field types are well defined.  
However, the licence is missing and the update frequency is not respected.

In conclusion, the dataset is technically easy to use, but its legal reliability remains limited.


# Final Synthesis: Recommended, Enforced and Used Practices on data.gouv.fr (IRVE datasets)

Based on 10 different datasets, it is possible to distinguish what is **recommended**, **enforced**, and **actually used in practice** regarding metadata, formats, and schemas.


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


## 4. Overall Conclusion

In conclusion, **data.gouv.fr** provides a strong framework for open data standardization.  
Formats and schemas are well defined and technically enforced for consolidation purposes.

However, the quality of metadata and governance still depends heavily on the producer.  
While institutional and professional actors generally follow best practices, others publish datasets with limited documentation and unclear reuse conditions.

Thus, the portal successfully encourages standardization, but full compliance remains uneven in practice.

