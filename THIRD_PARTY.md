# Public licence clarification

The author selected MIT for first-party software on 21 November 2026. The repository-root LICENSE supersedes the historical paragraph below that says the software licence was pending. No MIT grant is made for data, data-derived materials, model weights, external QA utilities or dependencies. Original producer terms remain applicable. The first DOI-assigned software record is [10.5281/zenodo.24427161](https://doi.org/10.5281/zenodo.24427161); its files and scope are described on the record page.

The following source-attribution document is preserved from the original software archive.

# Data sources and software attribution

## The authors' software

The Python pipeline, revision analyses and instructions prepared for this article are publicly archived. The first-party software is MIT licensed; the published Zenodo v1.0.3 record is [10.5281/zenodo.24427161](https://doi.org/10.5281/zenodo.24427161).

## Measurements and derived materials

| Source | Producer and terms | Materials in this archive |
|---|---|---|
| NOVIC+ | Yi et al. described the motor compound-fault measurements. The v2 part 1 deposit records CC BY 4.0. [Dataset](https://doi.org/10.5281/zenodo.15743425) · [Study](https://doi.org/10.1016/j.ymssp.2025.113786) · [Licence](https://creativecommons.org/licenses/by/4.0/) | File identifiers, proxy group/interval definitions, calculated feature values and study outputs. Obtain measurement arrays from the deposit. |
| HUSTbearing | Chao Zhao, Enrico Zio and Weiming Shen. The providers make their measurements available for validation of diagnostic algorithms and request citation of their study. [Provider README and citation request](https://github.com/CHAOZHAO-1/HUSTbearing-dataset/blob/554fe1269055660c41e9011fe97b971348bdec7f/README.md) · [Article](https://doi.org/10.1016/j.ress.2024.109964) | File names and source hashes, derived features and plotted examples, evaluation labels, predictions and trained models. Full raw spreadsheets and signal-patch archives must be obtained or reconstructed locally. |
| Paderborn | KAt DataCenter, Chair of Design and Drive Technology, Paderborn University. Cite Christian Lessmeier et al., *Condition Monitoring of Bearing Damage in Electromechanical Drive Systems by Using Motor Current Signals of Electric Motors: A Benchmark Data Set for Data-Driven Classification*, 2016. The producer specifies CC BY-NC 4.0. [Official dataset and conditions](https://mb.uni-paderborn.de/kat/forschung/bearing-datacenter) · [Article](https://doi.org/10.36001/phme.2016.v3i1.1577) · [Licence](https://creativecommons.org/licenses/by-nc/4.0/) | Source IDs and hashes, acquisition/patch lineage, and derived results from training and test allocations. The pipeline casts the vibration channel to float32, builds nominal and timestamp-derived time grids, computes features and aggregates model predictions. The third-party [Zenodo record](https://doi.org/10.5281/zenodo.15845309) supplied the specific source RARs. Its catalogue licence field differs from the original producer's terms. |

Data-source conditions continue to apply to covered materials independently of any licence later selected for the authors' software. Provider raw files, full-resolution waveform caches, and original Paderborn bearing-profile PDFs are distributed by their respective sources.

## External software

The optional MFoS2E benchmark imports upstream code from the pinned [MFoS-2-E revision](https://github.com/SRISLAB/MFoS-2-E/tree/bd84cf9168b44b7ad56a20859e0a40438a005549). The source manifest lists the required names, download URLs and SHA-256 values. The archive supplies the study adapter and computed tables. The ClassBD pilot uses the study's paper-guided implementation. The upstream [ClassBD revision](https://github.com/asdvfghg/ClassBD/tree/08530497e388ed691936f15d6c55267f277ed270) is credited in the vendor provenance manifest. Both vendor directories contain provenance only. Dependencies installed from package managers retain their own licences.
