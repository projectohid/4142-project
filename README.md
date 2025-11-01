# EEG Signal Analysis using Digital Signal Processing Techniques

## 📘 Overview
This project applies **Digital Signal Processing (DSP)** techniques to analyze and interpret **Electroencephalogram (EEG)** signals, focusing on the detection and characterization of **epileptic seizure activity**.  
It demonstrates how classical DSP methods such as filtering, Fourier Transform, Power Spectral Density (PSD), entropy, and correlation analysis can be systematically applied to biomedical data for meaningful interpretation and feature extraction.

---

## 🎯 Objectives
- To preprocess EEG signals using DSP filters for noise and artifact removal.  
- To perform frequency-domain analysis using FFT and PSD.  
- To extract statistical and nonlinear features (kurtosis, skewness, entropy).  
- To compare normal and seizure EEG patterns through visualization and quantitative metrics.  
- To establish DSP-based features as a foundation for machine learning–driven seizure detection.

---

## 🧠 Methodology
1. **Data Acquisition:**  
   EEG datasets containing normal and seizure segments were used for analysis.  

2. **Preprocessing:**  
   - Notch filter at 60 Hz to remove powerline interference.  
   - FIR bandpass filter (0.5–70 Hz) to isolate relevant brainwave frequencies.  

3. **Spectral Analysis:**  
   - Fast Fourier Transform (FFT) and Power Spectral Density (PSD) estimation.  
   - Spectrograms to visualize time–frequency energy distribution.  

4. **Feature Extraction:**  
   - Time-domain: Mean, variance, skewness, kurtosis.  
   - Frequency-domain: Band power across δ, θ, α, β, γ bands.  
   - Nonlinear: Spectral entropy, inter-channel correlation coefficients.  

5. **Visualization:**  
   Multiple plots illustrate raw and filtered signals, frequency spectra, spectrograms, entropy–power relationships, and correlation feature trends.

---

## 📊 Results Summary
- Filtering successfully removed baseline drift and 60 Hz noise while retaining physiological EEG components.  
- FFT and PSD analyses revealed low-frequency dominance (0–10 Hz) during seizures.  
- Entropy analysis showed decreased complexity and higher synchronization in seizure states.  
- Correlation plots indicated strong inter-channel coherence during epileptic episodes.  
- Extracted features demonstrated clear separation between normal and seizure EEG signals.

---

## 🧩 Discussion & Conclusion
The results confirm that DSP provides an effective, interpretable framework for EEG signal analysis.  
Filtering, spectral decomposition, and feature extraction jointly reveal both **temporal** and **spectral** characteristics of seizure activity.  
The extracted DSP-based features are physiologically meaningful and ready for integration into **machine learning** models for automated seizure detection.

---

## 🧰 Requirements
To run the code, ensure the following dependencies are installed:

```bash
pip install numpy scipy matplotlib pandas
