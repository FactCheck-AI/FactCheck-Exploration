# FactCheck web platform

> **Research use only. Not a medical device.**
> This software was developed in the HEREDITARY project as a research prototype. It has not been assessed or certified under the EU Medical Device Regulation (EU) 2017/745. It must not be used to diagnose, treat, monitor or make any other decision about individual patients.

## 1. Overview

| Field | Value |
|---|---|
| Name | FactCheck web platform (FactCheck-Exploration and FactCheck-Exploration-Backend) |
| Version | No tagged version (main branch) |
| Type | Demo or web application |
| Owner partner and contact | University of Padua (UNIPD), Stefano Marchesin, stefano.marchesin@unipd.it |
| License | MIT (see LICENSE file) |
| Repository and DOI | https://github.com/FactCheck-AI/FactCheck-Exploration and https://github.com/FactCheck-AI/FactCheck-Exploration-Backend (no Zenodo DOI); deployed at https://factcheck.dei.unipd.it |
| Release date | 27 November 2024 (front end), 17 December 2024 (back end); last update 18 February 2025 |
| Related task or deliverable | T4.1 |
| How to cite | F. Shami, S. Marchesin and G. Silvello. Fact Verification in Knowledge Graphs Using LLMs. Proc. 48th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2025, Padua, Italy, pp. 3985-3989. ACM, 2025. doi:10.1145/3726302.3730142 |

## 2. Intended use

**Primary intended use.** Web platform to inspect how FactCheck verifies KG facts. For each fact of the DBpedia and YAGO datasets it shows the questions generated from the triple, the web evidence retrieved, the prompts, and the verdicts of several LLMs with their agreement. Signed-in users can leave feedback on a verdict. It supports research and teaching on LLM-based fact verification.

**Intended users.** Researchers, students and developers interested in KG fact verification.

**Out-of-scope uses.** This release must not be used for
- clinical diagnosis, prognosis or treatment of individual patients;
- decisions about individuals, such as insurance, employment or access to care;
- re-identification of individuals or linkage with other data sources;
- populations, devices or data types not described in Section 3;
- use of the displayed verdicts as authoritative fact checks.

## 3. Data provenance

| Dataset | Source partner | Type (public, synthetic, pseudonymized, anonymized) | Population (size, age, sex, country, condition) | Ethics approval or access conditions |
|---|---|---|---|---|
| Pre-computed verification results (questions, prompts, LLM outputs) for DBpedia and YAGO facts | UNIPD, FactCheck benchmark | Public | Not applicable (KG triples; no human population) | Released with the front end |
| Web evidence (page text and HTML) retrieved through Google Search | External: publicly accessible web pages | Public | Not applicable | Third-party content; terms of the original websites apply |

This repository and the released files contain no personal data, pseudonymized records, identifiers or pseudonymization keys.

## 6. Known limitations and risks

- **Generalizability.** The platform displays pre-computed results for the facts of the two datasets; it does not verify new facts.
- **Known biases and confounders.** A fact is considered true if the KG snapshot supports it. LLMs may be biased towards "true" on highly accurate KGs such as YAGO.
- **Failure modes.** Retrieved web evidence can be noisy, outdated or unrelated to the fact, and LLM verdicts can disagree across models.
- **Privacy risks.** No trained model. The deployed back end stores optional user accounts (email, username, avatar URL, Google or ORCID identifier) and the feedback entered by signed-in users; these data are not part of the repositories.

## 7. Responsible use and reporting

- **Terms of use.** MIT license. Research use only, as stated in the disclaimer above.
- **Contact for misuse or vulnerability reports.**

## 8. Acknowledgement

Funded by the European Union under grant agreement No 101137074 (HEREDITARY). Views and opinions expressed are however those of the author(s) only and do not necessarily reflect those of the European Union or the European Health and Digital Executive Agency (HaDEA). Neither the European Union nor the granting authority can be held responsible for them.
