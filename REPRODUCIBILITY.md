# Reproducing the analyses

Download the four computational assets from release v2026.11.21. Check SHA256SUMS.txt before extraction. Keep the base ZIP and an unchanged extracted base directory. Run calculations in separate working outputs as instructed in each README.

## Base archive
Extract bearing_diagnosis_software_v1.0.2.zip and open a shell at its root.

~~~text
python -m pip install -r requirements-replay.txt
python scripts/v8/verify_saved_results.py
python scripts/revision/verify_source_selection.py
python scripts/revision/principal_tables.py verification/tables
~~~

The complete README lists acquisition, hashes, partitions, dependencies, training and evaluation commands. Download original data only from the documented providers under their terms. Historical output directories must not be mistaken for new fits.

## S29
Extract hust_weighting_analysis_source.zip, then:

~~~text
python hust_weight_sensitivity.py --software-zip source_data.zip --output outputs
~~~

This reweights fixed predictions; it is not an independent-bearing experiment.

## Add-on
Extract revision_strengthening_v1.1.1_public.zip. Read PUBLIC_RELEASE_NOTES.md before the historical README.

~~~text
python scripts/check_base_inputs.py --project EXTRACTED_BASE --archive bearing_diagnosis_software_v1.0.2.zip
~~~

Follow its portable CLI instructions to rebuild source inputs, pair frozen checkpoints or run the 30-fit normalization comparison. Source data downloads are separate actions. Historical executable evidence scripts contain deidentified location placeholders; use the portable scripts/ entry points.

## Current figures
Extract Figure_sources_v3_public.zip. Reconstruct the HUST patch cache using the add-on before recreating two excluded illustration files:

~~~text
python restore_waveform_inputs.py --base EXTRACTED_BASE --patches REBUILT_HUST/hust_neural_patches.npz --figures .
~~~

Then run the entry point from each corresponding directory:
- figure1: python draw_figure1_v3.py
- main_figures: python render_main_v3.py
- si_early: python redraw_si_early.py
- si_late: python render_all.py

Use Python 3.10 and the package versions documented in the archives. NumPy, SciPy, pandas, Matplotlib, Pillow and PyMuPDF are used; Arial is needed for the verified typography. External QA utilities are not redistributed. Their absence is reported as SKIPPED, not PASS; historical QA records retain their original scope.

## What was actually verified
The public figure helper was tested on the previously reconstructed local HUST cache, not by repeating network acquisition. All 10 arrays were identical; all 23 fresh public exports matched current PDF text and 72-dpi pixels. Numeric CSVs and checkpoints retained in the public variants are byte-identical to their originals. The release preparation did not rerun all historical training.

Original archive manifests and embedded execution hashes identify historical bytes. For deidentified public variants, use PUBLIC_SHA256SUMS.json and PUBLIC_RELEASE_MAPPING.json. Do not overwrite historical hashes to disguise differences.
