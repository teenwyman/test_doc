---
layout: default
title: UKB GP Provider
nav_order: 3
parent: UKB GP
grand_parent: UKB
description: "Provider mapping from UK Biobank Primary Care(GP) data"
---

# CDM Table name: PROVIDER

## Reading from UKB.lookup626, CDM.Care_Site
Using a dummy code: ***'GP-' + care_site_name*** derived from CDM Care Site to represent General Practice in UKBiobank.
The GP location is present by linking it to CDM Care_Site and CDM Location. 

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| provider_id | care_site_id | | |
| provider_name | | | NULL |
| npi | | | NULL |
| dea | | | NULL |
| specialty_concept_id | | [38004446 - General Practice](https://athena.ohdsi.org/search-terms/terms/38004446)|
| care_site_id | care_site_id | |
| year_of_birth | | | NULL | 
| gender_concept_id | | | NULL |
| provider_source_value | | CONCAT('GP-', care_site_name) |
| specialty_source_value | 'General Practice' | |
| specialty_source_concept_id | | | NULL |
| gender_source_value | | | NULL |
| gender_source_concept_id | | | NULL |