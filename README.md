# Arabic translation of the Human Phenotype Ontology (HPO)

This repository contains tools and data for the Arabic translation of the Human Phenotype Ontology (HPO). 

### Disclaimer
This is not the official version of the HPO Arabic translations. The official HPO translations and the official translation process are managed by the HPO consortium and can be found at:
[https://obophenotype.github.io/hpo-translations/translations/](https://obophenotype.github.io/hpo-translations/translations/)

This repository represents an independent effort (PAVS project) to provide high-quality Arabic mappings for clinical phenotypes.

## Translation Principles
This Arabic version of the HPO was built following strict clinical and linguistic principles to ensure accuracy and consistency:

1.  **Clinical Precision**: We prioritize established Arabic medical terminology used in clinical practice across the Middle East.
2.  **Structural Consistency**: Terms are translated following a systematic pattern, typically stating the abnormality first followed by the anatomical location (e.g., `[Abnormality] + في + [Location]`).
3.  **Contextual Awareness**: Translations are generated and reviewed using the full context of the HPO, including English definitions, synonyms, and hierarchical (parent/child) relationships to resolve ambiguities.
4.  **Linguistic Standard**: We use Modern Standard Arabic (MSA) to ensure broad accessibility and compatibility with standardized medical databases.
5.  **Hybrid Workflow**: We employ a "Human-in-the-loop" approach, utilizing advanced LLMs (GPT-4o) for initial high-fidelity mapping followed by expert clinical review.

## License
The Arabic translations and the software tools provided in this repository are licensed under the **[Creative Commons Attribution 4.0 International (CC-BY 4.0)](LICENSE)** license.

**Note:** This license applies specifically to the Arabic translation work and the scripts in this repository. The original Human Phenotype Ontology (English) is subject to its own [licensing terms](https://hpo.jax.org/app/license).

## Contents

- `hp-ar.obo`: HPO in OBO format with Arabic synonyms and definitions.
- `hp-ar.babelon.tsv`: Translations in Babelon format.
- `hpo_arabic_translations.json`: The raw LLM-generated translation cache.
- `scripts/`: Tools for translation, validation, and export.

## Tools

### 1. `translate_hpo_ar.py`
The core translation script using LLMs (GPT-4o via OpenRouter).
- **Batching**: Processes multiple terms per API call.
- **Resume Support**: Detects existing translations and skips them.
- **Contextual Translation**: Provides the LLM with full definitions and hierarchical context.

### 2. `export_results.py`
Converts JSON output into distribution formats (OBO, TSV, etc.).

## Translation Conventions

### 1. Arabic Sentence Structure Examples
- *Fingernail hypoplasia* → نقص تنسج في أظافر اليد
- *Renal tubular dysfunction* → خلل في الأنابيب الكلوية

### 2. Medical Glossary (Key Terms)
| English | Arabic |
| :--- | :--- |
| Metaphysis | كردوس |
| Epiphysis | مشاشة |
| Dysplasia | خلل تنسجي |
| Hyperplasia | فرط تنسج |
| Atrophy | ضمور |

---
**Maintained by:** Bio-Ontology Research Group (BORG)
**Part of Project:** PAVS (Phenotypic and Variant Standardization)
