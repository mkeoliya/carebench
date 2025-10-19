# CAREBench

1. Set up MEDS dataloaders for EHRShot, MC-MED and MIMIC-IV. Pending: rest of MEDS data.
2. Set up `Dataset` class which can take in a MEDS dataset, a target outcome, horizon (`h`), and window size (`t`), and produce `X, y` labels.
   - Ensure that class can take in any modality: Tabular (EHR), waveforms (ECG, PPG), Image (JPG), Text. 
4. Implement `Model` class which can consume `Dataset` class. Implement: DT, RF, LSTM, RNN, Transformer, LLMs interface. 
5. Set up metrics, which can take in the output of `Model` and measure: AUROC, AUPRC, Calibration, Robustness (data-dropping), Stability.
6. Set up `Explainer` class which explains the predictions of a `Model` on a `Dataset` at a given timestamp. E.g. `SHAP`, .... 
7. Ablations: Vary horizon, Cross-Task Generalizability, Vary Tokenization Schema, Perturbation 
