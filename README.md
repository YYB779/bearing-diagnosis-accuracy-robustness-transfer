# Separating diagnostic accuracy from robustness and transfer in bearing fault diagnosis

Software and computational evidence accompanying the research manuscript by **Zongyuan Yang**.

This repository separates clean diagnostic accuracy, synthetic-disturbance stability and frozen cross-dataset transfer across NOVIC+, HUSTbearing and Paderborn. It documents controlled comparisons and their limitations; it does not introduce a new diagnostic architecture or establish industrial reliability.

## Start here

- [Versioned release materials](https://github.com/YYB779/bearing-diagnosis-accuracy-robustness-transfer/releases/tag/v2026.11.21)
- [Source-only snapshot](repository_source.zip): 122 Python files, instructions and software licence. Extract it to inspect preserved relative program paths; large inputs, frozen predictions and checkpoints are in the release assets.
- [Reproduction guide](REPRODUCIBILITY.md)
- [Public distribution changes](PUBLIC_RELEASE_NOTES.md)
- [Source attribution and data conditions](THIRD_PARTY.md)
- [File digests](SHA256SUMS.txt)

Use these four computational assets together:

| Asset | Purpose |
|---|---|
| bearing_diagnosis_software_v1.0.2.zip | Original preprocessing, feature extraction, training/evaluation scripts, partitions, saved predictions and checkpoints |
| hust_weighting_analysis_source.zip | S29 fixed-prediction weighting sensitivity |
| revision_strengthening_v1.1.1_public.zip | Raw-input reconstruction, same-checkpoint diagnostics and paired-normalization experiment |
| Figure_sources_v3_public.zip | Seven current main figures and supplementary Figures S1–S16; includes a local waveform reconstruction helper |

The base README preserves the historical numbering of eight submitted main figures. The current manuscript uses seven main figures and S1–S16; the current figure-source asset supplies that layout.

## Scope and verification

The original measurements remain with their providers. The public figure asset excludes two short HUST waveform NPZ files and external QA utilities whose redistribution licence was not recorded. The supplied reconstruction helper reproduced all ten original illustration arrays exactly from the independently rebuilt local HUST patch cache. Four public figure entry points exported all 23 figures; extracted text and 72-dpi raster output matched the manuscript-v6.4 figures exactly. External layout audits are explicitly SKIPPED when their utilities are absent.

Algorithm seeds, repeated acquisitions and patches are not independent physical specimens. Physical IDs remain incomplete in NOVIC+/HUST, the nine Paderborn test bearings include only three healthy specimens, and manufacturer is confounded with health. Synthetic disturbances and retrospective extensions do not establish prospective field reliability.

## Licence and citation

[MIT](LICENSE) applies to first-party software. It does not grant MIT rights in datasets, derived data, model weights or external dependencies; [provider terms](THIRD_PARTY.md) remain applicable. In particular, covered Paderborn material retains the producer's CC BY-NC 4.0 conditions.

Use [CITATION.cff](CITATION.cff) to cite the software and cite the original data providers. No software DOI is claimed until a DOI-assigning repository deposit is actually published. The repository contains no journal reviewer report, response letter or editorial correspondence.
