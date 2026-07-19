# AI in EMC: A Systematic Literature Corpus

Curated and annotated corpus of research articles on the use of **artificial intelligence in electromagnetic compatibility (EMC)** and adjacent electromagnetic domains. This dataset accompanies the review article *"Artificial Intelligence in Electromagnetic Compatibility and Related Electromagnetic Domains: A Systematic Review"* (in preparation, target venue: IEEE Access).

## Corpus at a glance

| Stage | Count |
|---|---|
| PDF records collected (2024–2026, last search July 2026) | 382 |
| Duplicates removed (MD5 / DOI / fuzzy-title matching) | 13 |
| Unique documents screened | 369 |
| **Core layer — AI applied to EMC problems** | **123** |
| **Adjacent layer — AI in EMC-related EM domains** | **162** |
| Excluded (EMC without AI / AI without EMC / out of scope) | 84 |

Publication years span 2012–2026 (core layer) and 2019–2026 (adjacent layer).

## Files

| File | Content |
|---|---|
| `data/core_ai_in_emc.csv` | 123 articles using AI for EMC problems: first author, year, title, EMC category (A–E), AI category (1–5), concrete AI technique, review flag, core claim, results, limitations, source file name |
| `data/adjacent_ai_in_em.csv` | 162 articles using AI in EMC-related EM domains (antennas, microwave filters, metasurfaces, propagation, computational EM): EM category (F1–F5), AI category, technique, review flag, annotations |
| `Analyza_clanku_AI_v_EMC.xlsx` | Full analysis workbook (tables, statistics, cross-tabulations, methodology) |

## Taxonomy

**EMC categories (core layer):**
- **A — Shielding and EMC materials:** shielding-effectiveness prediction and design, shielding composites, FSS/metasurface shields, microwave absorbers, magnetic shielding, WPT shielding, enclosures and apertures
- **B — EMI/emission modeling and prediction:** conducted and radiated emissions, converter EMI, EMI filters, equivalent source models, surrogate EM simulation for EMC assessment
- **C — EMC testing, measurement and diagnostics:** near-field scanning, source localization, test acceleration, reverberation and anechoic chambers, interference classification, EMI cancellation in measurement
- **D — Signal and power integrity (SI/PI):** power delivery networks, decoupling capacitors, interconnects and vias, crosstalk, eye diagrams, PCB stack-up
- **E — System-level EMC, immunity and exposure:** susceptibility (EMS), coupling to cables, SAR and human exposure, EM environment, EMC knowledge management, antenna decoupling for interference reduction

**EM categories (adjacent layer):** F1 — Antennas and antenna arrays; F2 — Microwave filters and circuit components; F3 — Metasurfaces, FSS and absorbers (non-shielding); F4 — Wave propagation, channels and communication systems; F5 — Computational electromagnetics and EM modeling.

**AI categories (both layers):** 1 — Neural networks and deep learning (ANN/DNN/CNN/RNN/GNN/PINN); 2 — Classical machine learning (SVM, random forests, kNN, Gaussian processes, ensembles); 3 — Generative and inverse models (GAN, (c)VAE, diffusion, tandem/inverse networks); 4 — Reinforcement learning; 5 — Metaheuristics and Bayesian optimization (GA, PSO, DE, BO).

For combined approaches (e.g., DNN surrogate + genetic algorithm), the article is assigned to the family constituting its main contribution; the concrete combination is preserved in the `ai_technique` column. A post-hoc consistency audit of the AI-family labels led to four reassignments (inverse-design networks in the shielding category); the CSV files contain the audited labels used in the article.

## Methodology summary

Articles were collected over two years (2024–2026) by a five-member team (AI specialist; two EMC researchers — shielding/simulation and shielding; antenna researcher; EMC industry practitioner; a senior advisor performed final checks). Primary source: Google Scholar (chosen for its coverage of venues beyond WoS/Scopus, including conference workshops and preprints), complemented by backward/forward snowballing from review articles and expert recommendations gathered at EMC Europe and IEEE EMC+SIPI, and within the PATTERN doctoral network on AI in EMC. Classification disagreements were resolved by discussion, with the first author adjudicating. Deduplication used MD5 file hashes, DOI matching, and fuzzy title matching (similarity > 0.90) with manual verification of borderline cases. Peer-reviewed publications and preprints in English were eligible; ionizing-radiation shielding was excluded as out of EMC scope.

## License

This dataset is released under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license. You are free to share and adapt the material for any purpose, provided appropriate credit is given.

The dataset contains bibliographic metadata and original annotations only; it does **not** redistribute the full texts of the analyzed articles.

## How to cite

See `CITATION.cff`. A Zenodo DOI will be minted upon release; until then, please cite the GitHub repository and the accompanying article once published.
