# Interpretable Remaining Useful Life (RUL) Predictions Using Temporal SHAP

## Introduction
This project tackles the challenge of explaining deep‑learning Remaining Useful Life (RUL) predictions for aircraft engines. We adapt a Long Short‑Term Memory (LSTM) regressor (window = 20 time‑steps × 16 features) and pair it with TimeSHAP, a temporal extension of SHAP, to expose when and which sensor readings drive each prediction. TimeSHAP outperforms vanilla SHAP‐on‑flattened‑data by revealing time‑dependent feature effects, providing rich insights and benefits to RUL predicitions.

## Project Metadata
### Authors
- **Author:** Nawaf Altahini
- **Supervisor Name:** Dr. Muzammil Behzad
- **Affiliations:** KFUPM

### Project Documents
- **Presentation:** [Project Presentation](/presentation.pptx)
- **Report:** [Project Report](/Interpretable%20Remaining%20Useful%20Life%20(RUL)%20Predictions%20Using%20Temporal%20SHAP.pdf)

### Reference Papers
- Peringal A., Mohiuddin M. B., Hassan A. (2024) Remaining Useful Life Prediction for Aircraft Engines Using LSTM
- Lundberg S. M., Lee S‑I. (2017) A Unified Approach to Interpreting Model Predictions
- Bento J. et al. (2021) TimeSHAP: Explaining Recurrent Models through Sequence Perturbations

### Reference Dataset
- [C-MAPSS Dataset (FD001)] (https://data.nasa.gov/Aerospace/CMAPSS-Jet-Engine-Simulated-Data/ff5v-kuh6/about_data)


## Project Technicalities

### Terminologies
Term	Brief Definition
- **RUL:** Cycles remaining before engine failure.
- **LSTM:**	Recurrent layer capturing temporal dependencies.
- **Window:**	Fixed‑length sequence fed to the network.
- **SHAP Value:**	Shapely Additive Explanation Value; Attribution of a feature to a single prediction.
- **TimeSHAP:**	SHAP variant that perturbs sequences to preserve temporal context.

### Problem Statements
- **Problem 1:** Complex RUL models restrict user trust and adoption, thus requiring interpretation.
- **Problem 2:** Interpretation technique SHAP flattens time‑series data, losing temporal insight.

### Problem vs. Ideation: Proposed 2 Ideas to Solve the Problems
1. **Time Aware XAI Integration:** Apply TimeSHAP to retain temporal context in attributions.
2. **Systematic Analysis and Clear Visualization** Provide heatmaps and waterfall plots for intuitive insights in a systematic approach.

### Proposed Solution: Code-Based Implementation
This repository provides an implementation of the above ideas. The solution includes:

- **TimeSHAP Implementation:** Incorporates TimeSHAP along with SHAP for comparasion.
- **Waterfall and Heatmaps Visualizations:** Visualize TimeSHAP and SHAP Values to assess explainability.

## Acknowledgments
- **Open-Source Communities:** Thanks to the contributors of TimeSHAP, SHAP, PyTorch, and other libraries for their amazing work.
