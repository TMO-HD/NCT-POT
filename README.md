# NCT Precision Oncology Thesaurus (NCT-POT) and NCT Data Space (NCT-DS)
Ontology for Precision Oncology Workflows at the National Center of Tumor Diseases Heidelberg

# Background
With the ongoing **transformation of conventional oncology into a data-driven science**, and a rising number of cancer patients undergoing comprehensive OMICs assessments (whole-genome/exome sequencing, transcriptome sequencing, methylome, proteomics, ...), precision oncologists face two critical **challenges**:
  
1. Increase the **scalability of existing clinical workflows** (e.g. in molecular tumor boards, MTBs), thereby allowing assessment of best therapeutic options for more patients in less time and with high(er) quality
2. **Speed up the scientific analysis** of clinic-molecular data of cancer patients, thereby gathering new scientific insights

A part of the solution to these challenges is **strong semantic tagging** of both patient-related and non-patient-related data. There are a lot of published taxonomies available for different data domains in precision oncology (e.g. diagnoses, drugs, therapies, molecular markers etc.), however they frequently **lack sufficient integration**. Besides, for certain domains (e.g. drug classes) the **available taxonomies** are **not sufficient** at all from the clinical perspective.

# Aims
The NCT aims to support precision oncology workflows by providing: 
1. **NCT Data Space**: A data concept for organizing both patient-related and non-patient-related data for precision oncology workflows. 
2. **NCT Precision Oncology Thesaurus**: An integrated ontology embracing a growing number of data domains relevant for precision oncology workflows, e.g. clincal information regarding diagnoses, diagnostics and therapies as well as (molecular)biological/pharmaceutical like drugs (and their classes), drug targets, molecular alterations etc. It integrates both establishes external taxonomies and self-maintained 

# NCT Data Space
To be added.

# NCT Precision Oncology Thesaurus (NCT-POT)
## NCT-POT: Overview
Technically, the NCT-POT is implemented as a relational database with tables and links between tables. Generally speaking, we habe three types of tables:
- **External Source Tables**: Importing relevant information from external taxonomies that can be updated (semi-)automatically periodically
- **NCT-POT Integration Tables**: Referencing mapping entries from several external taxonomies, possibly providing added information. 
- **NCT-POT MASTER Tables**: Representing self-maintained proprietory taxonomies

![image](https://user-images.githubusercontent.com/5072766/171009917-7a33f2c2-4738-4cbf-8b61-98993fe50034.png)
Illustration of the data flow in a part of the NCT Precision Oncology Thesaurus. Data from different external taxonomies is periodically used to update NCT-POT and to provide links to the external taxonomies. The linkage between the tables of the diverse data domains is mainly a result of manual curation (see below).

## NCT-POT: Data Domains
Currently there are data tables 

## NCT-POT: Entity-Relationship-Model



## NCT-POT: Sources
Diagnoses
- [OncoTree](http://oncotree.mskcc.org)

Drugs
- [NCI Thesaurus](https://ncithesaurus.nci.nih.gov/)
- [Hemonc.org](https://hemonc.org/)
- [FDA](https://www.accessdata.fda.gov/scripts/cder/daf/)
- [DrugBank](https://go.drugbank.com/)

Molecular Targets
- [HGNC](https://www.genenames.org/)
- [UniProtKB](https://www.uniprot.org/)
- [Ensembl](http://www.ensembl.org)

## NCT-POT: Manual Curation
Data from all sources is periodically updated (usually monthly) from their primary sources and integrated into the NCT-POT, thereby updating the NCI-POT master tables. Links between different data domains are manually curated by a team of dedicated scientist and oncologists actively involved in precision oncology workflows within the NCT network.

## NCT-POT: Download and License
### NCT Precision Oncology Thesaurus
Data can be downloaded here.  

Updates of the NCT Precision Oncology Thesaurus are provided monthly.

All data is published under the ??? license.

# Feedback
We are happy to collect feedback to our work (critics and compliments, corrections and suggestions for improvements) here.
