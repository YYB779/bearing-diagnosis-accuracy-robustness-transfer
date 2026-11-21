# Public release notes: v2026.11.21

This collection corresponds to manuscript v6.4. It combines an unchanged base software 1.0.2, unchanged S29 analysis, public distribution of add-on 1.1.1, and public distribution of figure sources v3. The manuscript version and individual software component versions are distinct.

The base and S29 archive bytes are unchanged. The two public variants replace author-machine paths with placeholders; their PUBLIC_RELEASE_MAPPING.json records original and public member hashes. Historical execution digests remain historical; PUBLIC_SHA256SUMS.json covers the public variant.

The author selected MIT for first-party code. This supersedes historical software-licence-pending wording in preserved READMEs and THIRD_PARTY.md. It does not relicense data, derived data, model weights or external dependencies.

The public figure asset excludes:
- si_early/inputs/S4_training_views.npz
- si_late/data/frozen_s9_signals.npz
- 13 externally supplied qa_tools/*.py files whose redistribution licence was not recorded.

No model checkpoint or numerical CSV is modified by the public conversion. The two excluded illustration files can be reconstructed locally from provider-derived HUST inputs using restore_waveform_inputs.py. All ten original arrays matched exactly in the local verification. The optional external-QA adapter records SKIPPED when no utilities are present. Four public drawing entry points produced all 23 current figures with text and 72-dpi raster equality to the manuscript-v6.4 PDFs.

The base README's eight-figure numbering is historical. The current figure asset supplies seven main figures and S1–S16. The public source-only snapshot supplies 122 Python files in their component-relative directories; execution requires the complete assets.

The software and figure-source materials are archived in the published Zenodo record [10.5281/zenodo.24427161](https://doi.org/10.5281/zenodo.24427161), version 1.0.3, which retains the v1.0.2 software archive and includes the repository snapshot and revision-strengthening package. The GitHub release additionally provides the HUST weighting-analysis archive; journal submission remains a separate author action.
