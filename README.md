# MeLiDos IZTECH GLC dataset

This repository contains the Izmir Institute of Technology (IZTECH) site data from the MeLiDos field study, refactored as a GLC Schema 3.0.1 Data Package and derived from the [original MeLiDos dataset](https://github.com/MeLiDosProject/DidikogluEtAl_Dataset_2025).

The package entry point is `datapackage.json`. Core study, participant, device, datasheet, dataset, and variable metadata are stored in `data/`; the participant-level CSV files referenced by `data/datasets.json` are organized as:

- `data/files/sensor/`: participant-level head, chest, and wrist sensor tables;
- `data/files/longitudinal-reports/`: diaries, experience and wear logs, and repeated assessments;
- `data/files/questionnaires/`: screening, baseline, and end-of-study questionnaires;
- `data/files/study-timing/`: participant trial-period records.

The source dataset is:

> Didikoglu, A., Akgun, S. G., Aydin, S. N., Kayar, Z., Zauner, J., & Spitschan, M. (2025). *Personal light exposure dataset for Izmir, Türkiye*. https://doi.org/10.5281/zenodo.16568109

The refactoring converts the imported tabular RData resources to UTF-8 CSV, separates records by participant, and supplies GLC 3.0.1 metadata without modifying the source repository.

## Validation

Validation runs automatically through `.github/workflows/validate-glc-dataset.yml`. Successful runs produce an attested `validation-report` artifact containing `validation.json` and `validated-files-manifest.json`.

## License

The dataset is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0). See `LICENSE`.
