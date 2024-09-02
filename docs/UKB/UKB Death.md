---
layout: default
title: UKB Death
nav_order: 2
parent: UKB
has_children: true
description: "UK Person"
---

# CDM Table name: PERSON

## Reading from UKB.baseline

![](images/image02.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| person_id | eid | | |
| death_date | p31 | p31 will be mapped to Gender Concept_id by using UK Biobank vocabulary. | [Data-Field 31](https://biobank.ndph.ox.ac.uk/ukb/field.cgi?id=31) |
| death_datetime | p34 | |[Data-Field 34](https://biobank.ndph.ox.ac.uk/ukb/field.cgi?id=34) |
| death_type_concept_id | p52| | [Data-Field 52](https://biobank.ndph.ox.ac.uk/ukb/field.cgi?id=52) |
| cause_concept_id | cause_icd10 | cause_icd10 will be mapped to SNOMED Concept_id by using UKB_DEATH_CAUSE_STCM and ICD10 | It does not allow multiple death records for a single person in CDM Death. However, some ICD10 codes map to multiple standard concepts in Athena. UKB_DEATH_CAUSE_STCM, an STCM-tailored vocabulary, contains the 1:1 mapping information between these codes and standard concepts. |
| cause_source_value | cause_icd10 | | |
| cause_source_concept_id | p21000 | p21000 will be mapped to Race Concept_id by using UK Biobank vocabulary. |[Data-Field 21000](https://biobank.ndph.ox.ac.uk/ukb/field.cgi?id=21000) |


