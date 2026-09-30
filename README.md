# ECG Analysis for Myocardial Infarction Risk Prediction

## Overview

This project presents a comparison between two models for ECG beats classification for healthy patients and patients with myocardial infarction.

The project was developed as part of my Master's thesis in Biomedical Engineering.

## Dataset

The analysis was based on the PTB Diagnostic ECG Database available through PhysioNet.

The original ECG recordings are not included in this repository.

## Methodology

The analysis included the following main steps:

- R-peak detection
- heartbeat segmentation
- classification of heartbeats into normal and myocardial infarction classes
- evaluation of classification performance
- comparison of results of two neural-network-based approaches

R-peaks were detected using an external implementation of the Pan–Tompkins algorithm. This implementation is not my original work.

The first classification model was implemented by me based on the corresponding publication.

For the second classification model, I used an existing implementation provided by the authors. I ran the model on my data and evaluated its performance.

## Results

Both models achieved high classification accuracy in distinguishing between
normal and myocardial infarction beats.

| Model | Accuracy | Sensitivity | Precision | Specificity | F1-score |
|------|----------|-------------|-----------|-------------|----------|
| Model 1 | 99.55% | 99.66% | 99.80% | 98.95% | 99.73% |
| Model 2 | 99.85% | – | – | – | 99.91% |

The notebook also includes a confusion matrix for the first model and a conclusion.

## Reproducibility

The notebook documents the methodology and presents the results obtained during
the original thesis work. The original ECG recordings and the external implementations are not included in this repository.
Therefore, the complete analysis cannot be reproduced from the repository alone.

## References

### Dataset

Bousseljot, R., Kreiseler, D., & Schnabel, A. (1995).
Nutzung der EKG-Signaldatenbank CARDIODAT der PTB über das Internet.
Biomedizinische Technik, Band 40, Ergänzungsband 1, p. 317.

PTB Diagnostic ECG Database v1.0.0, PhysioNet.
https://doi.org/10.13026/C28C71

Pollard, T., Moody, B. E., Lehman, L., Gow, B., Fernandes, C., Xie, C.,
Johnson, A., Mark, R. G., & Heldt, T. (2026).
PhysioNet as a global platform for biomedical research.
Nature Health, 1, 792–795.
https://doi.org/10.1038/s44360-026-00096-z

### External implementations

Pan–Tompkins QRS Detection implementation:
https://github.com/antimattercorrade/Pan_Tompkins_QRS_Detection

Model 2 implementation:
Lynda Starkus, Abnormal_ECG_Myocardial_infraction_cnn.
https://github.com/Lynda-Starkus/Abnormal_ECG_Myocardial_infraction_cnn

### Model references

Acharya, U. R., Fujita, H., Oh, S. L., Hagiwara, Y., Tan, J. H., & Adam, M.
(2017). Application of deep convolutional neural network for automated
detection of myocardial infarction using ECG signals.
Information Sciences, 415–416, 190–198.
https://doi.org/10.1016/j.ins.2017.06.027

Kachuee, M., Fazeli, S., & Sarrafzadeh, M. (2018).
ECG Heartbeat Classification: A Deep Transferable Representation.
2018 IEEE International Conference on Healthcare Informatics (ICHI), 443–444.
https://doi.org/10.1109/ICHI.2018.00092
