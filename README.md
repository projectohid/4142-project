\# 🧠 EEG Signal Processing and Feature Extraction for Seizure Detection



\## 📘 Overview

This project demonstrates the application of \*\*Digital Signal Processing (DSP)\*\* techniques for \*\*EEG-based epileptic seizure detection\*\* using the \*\*CHB-MIT Scalp EEG Database\*\*.  

It bridges classical DSP methods—filtering, convolution, correlation, and spectral analysis—with modern biomedical signal analysis in Python.



The work was developed as part of the \*\*EE 4135: Digital Signal Processing Laboratory\*\* course.



---



\## 🎯 Objectives

\- Apply core DSP concepts (FFT, FIR/IIR filtering, correlation, convolution) to EEG signals.  

\- Develop a \*\*preprocessing pipeline\*\* for noise removal and signal standardization.  

\- Extract \*\*spectral, statistical, and nonlinear features\*\* relevant to seizure detection.  

\- Prepare features for \*\*machine learning and neural network models\*\*.



---



\## 🧩 Methodology



\### 1. Data Acquisition

\- Dataset: \[CHB-MIT Scalp EEG Database](https://physionet.org/content/chbmit/1.0.0/)

\- Format: EDF (European Data Format)

\- Each file contains multi-channel EEG recordings from pediatric epilepsy patients.



\### 2. Preprocessing Pipeline

| Step | Description |

|------|--------------|

| \*\*Notch Filtering\*\* | Removes 60 Hz powerline interference using IIR filter. |

| \*\*Bandpass Filtering\*\* | FIR filter (0.5–70 Hz) isolates standard EEG frequency range. |

| \*\*Segmentation\*\* | EEG divided into overlapping 10-second epochs. |

| \*\*Normalization\*\* | Z-score standardization (zero mean, unit variance). |



\### 3. DSP Operations

\- \*\*Correlation Analysis:\*\* Inter-channel Pearson correlation to measure spatial dependencies.  

\- \*\*Convolution Smoothing:\*\* Moving average for temporal smoothing.  

\- \*\*Spectral Analysis:\*\* FFT \& Welch PSD for frequency-domain analysis.  

\- \*\*Feature Extraction:\*\* Band power, spectral entropy, skewness, kurtosis, correlation metrics, and band ratios.



\### 4. Implementation

\- Environment: \*\*Python 3.10\*\*, \*\*Jupyter Notebook\*\*

\- Libraries: `mne`, `numpy`, `scipy`, `pandas`, `matplotlib`

\- Output: `chb\_features.csv` — structured feature matrix (30+ features per epoch).



---



\## 📊 Results Summary



| Analysis Domain | Key Observation | DSP Technique |

|------------------|-----------------|----------------|

| \*\*Spectrograms\*\* | Low-frequency dominance in seizure epochs | STFT / Spectrogram |

| \*\*Filtering\*\* | 60 Hz noise \& drift removed | Notch + FIR Bandpass |

| \*\*Band Power\*\* | High Δ, θ power; reduced α, β, γ | FFT + PSD |

| \*\*Statistics\*\* | High kurtosis, low skewness | Time-domain analysis |

| \*\*Entropy\*\* | Negatively correlated with Δ power | Spectral Entropy |

| \*\*Correlation\*\* | High inter-channel synchronization | Pearson Correlation |



---



\## 🧠 Key Findings

\- Clean EEG signals achieved via notch and FIR bandpass filtering.  

\- Clear spectral distinction between \*\*normal\*\* and \*\*seizure\*\* states.  

\- Statistical and nonlinear features (kurtosis, entropy) capture seizure morphology.  

\- Strong spatial coupling across channels during seizures.  

\- Extracted features are \*\*ML-ready\*\* for classification and real-time detection.



---



\## 🚀 Future Work

\- Integrate \*\*wavelet-based filtering\*\* for adaptive noise suppression.  

\- Apply \*\*Independent Component Analysis (ICA)\*\* for artifact rejection.  

\- Train \*\*deep learning models\*\* (CNN, LSTM) on DSP-derived features.  

\- Develop a \*\*real-time seizure detection\*\* pipeline.



---



\## 📁 Repository Structure



---



\## ⚙️ Installation \& Usage



\### Clone the Repository

```bash

git clone https://github.com/projectohid/4142-project.git

cd 4142-project





