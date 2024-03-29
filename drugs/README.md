# NCT-POT Drugs

Part of the [**NCT Precision Oncology Thesaurus (NCT-POT)**](https://github.com/TMO-HD/NCT-POT).

## Summary

**NCT POT Drugs** is a data package covering **drug-related information** in the contxt of **precision oncology** workflows. It contains information about drugs, drug classes and drug targets, manufacturers and their drug products (trade names etc.), and approvals and approval-relevant biomarkers and appropriate diagnoses. Information is derived from a number of publicly available [**sources**](NCT_POT_Drugs#Sources_for_Assembly)**,** updated monthly and manually curated by a team of precision oncologists at the [**Divison of Translational Medical Oncology (TMO)**](https://www.dkfz.de/en/translationale-medizinische-onkologie/index.php) **at the** [**National Center for Tumor Diseases in Heidelberg**](https://www.nct-heidelberg.de/)**.** Data can be [**downloaded**](NCT_POT_Drugs#Download) free-of-charge under the [**CC-BY-NC 4.0 International license**](#License) **.**

> :warning: Though striving for best quality, **we cannot guarantee the absence of errors** or the lack of relevant information. The data is intended for application in a scientific context. It **must not be used for clinical decision-making** without decision verification by clinicians with appropriate experience in  precision oncology.

## Use Cases

NCT-POT Drugs must address frequent use cases like:

| Searching for     | Example of request                                                                                                                                                 |
|------------------------------------|------------------------------------|
| **Drugs**         | Search for all drugs targeting CLDN18.2, NECTIN4 or KRAS G12C                                                                                                      |
| **Trials**        | Search for all available clinical trials combining checkpoint inhibitors with FGFR2 inhibitors                                                                     |
| **Evidence**      | Search all available evidence in evidence databases (like CIVIC or OncoKB ) for efficacy of inhibitors of the PI3K/AKT/mTOR signaling pathway in colorectal cancer |
| **Approvals**     | Are there drugs approved for NECTIN4-directed therapies in cervical cancer?                                                                                        |
| **Manufacturers** | Search for manufacturers suitable for a trial combining RAS/RAF/MEK/ERK pathway inhibitors with SHP2 inhibitors?                                                   |

## Entity relationship model

![Entity relationship model](https://github.com/TMO-HD/NCT-POT/raw/main/drugs/docs/NCT-POT_Drugs_ERM.png)

## Drug classes structure

The drug classes are a hierarchal taxonomy, self-maintained by the TMO and focusing on their usage in precision oncology workflows.

![Drug classes structure](https://github.com/TMO-HD/NCT-POT/raw/main/drugs/docs/NCT-POT_Drugs_class_structure.png)

## Sources for assembly

| name                             | source url                                                                   | assembly tables                                      | comment                                                                       |
|------------------|------------------|------------------|------------------|
| **CIVIC Variant Types**          | <https://civicdb.org/variant-types/home>                                     | approvalBiomarker                                    | some items ot covered in the sequence ontology                                |
| **FDA Drugs**                    | <https://www.fda.gov/drugs/drug-approvals-and-databases/drugsfda-data-files> | drug, drugProduct, approval                          |                                                                               |
| **HGNC Genes**                   | <https://www.genenames.org/>                                                 | drugTarget, drugClass, drugTarget, approvalBiomarker |                                                                               |
| **NCI Thesaurus**                | <https://www.ebi.ac.uk/ols/ontologies/ncit>                                  | drug, drugTarget                                     | only (a subset of) nodes below NCIT_C1909 ("Pharmacologic Substance") is used |
| **NCT POT Drugs - drug classes** | <https://github.com/TMO-HD/NCT-POT/tree/main/drugs>                          | drugClass                                            | self-maintained at NCT Heidelberg                                             |
| **NCT POT Drugs - manufacturer** | <https://github.com/TMO-HD/NCT-POT/tree/main/drugs>                          | manufacturer                                         | self-maintained at NCT Heidelberg                                             |
| **Oncotree**                     | <http://oncotree.mskcc.org/>                                                 | approval                                             |                                                                               |
| **Sequence Ontology**            | <http://www.sequenceontology.org/>                                           | approvalBiomarker                                    | manually selected items                                                       |
| **Uniprot**                      | <https://www.uniprot.org/>                                                   | drugTarget, approvalBiomarker                        |                                                                               |

## Data curation process

To be added

## Roadmap {#roadmap}

| Date        | Task                                                       |
|-------------|------------------------------------------------------------|
| 2023-01-end | Major database update                                      |
|             | Completion of the approvals' biomarker and entity tagging. |
| 2023-02-end | EMA approval integration                                   |
|             | hemonc.org integration                                     |
| monthly     | Updates from sources                                       |
| continously | Manual curation                                            |

## Download

**NCT POT Drugs** is released monthly.

| Date       | RData                                                               | TSV                                                               | Onkostar®                                                                             |
|---------------|---------------|---------------|---------------|
| 2023-01-10 | [Download](https://github.com/TMO-HD/NCT-POT/tree/main/drugs/RData) | [Download](https://github.com/TMO-HD/NCT-POT/tree/main/drugs/tsv) | [Download](https://github.com/TMO-HD/NCT-POT/tree/main/drugs/onkostarPropertyCatalog) |

## License

NCT POT Drugs is released under the [**CC-BY-NC 4.0 International license**](https://creativecommons.org/licenses/by-nc/4.0/) and is free-of-charge usable in a non-commercial environment. 

Please send us a short [**mail**](Mailto:simon.kreutzfeldt@nct-heidelberg.de) if you intend to use the content of NCT-POT drugs.

## Feedback

We are happy about any kind of feedback! 🙂

Please report via [**mail**](Mailto:simon.kreutzfeldt@nct-heidelberg.de) or in the [**issues section**](https://github.com/TMO-HD/NCT-POT/issues) on Github.

## Publications

-   Simon Kreutzfeldt, Alexander Knurr, Daniel Hübschmann, Peter Horak, Stefan Fröhling, **NCT Precision Oncology Thesaurus Drugs -- a Curated Database for Drugs, Drug Classes, and Drug Targets in Precision Cancer Medicine**; medRxiv 2022.09.11.22279783; doi: [doi.org/10.1101/2022.09.11.22279783](https://doi.org/10.1101/2022.09.11.22279783)
