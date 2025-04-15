# 🎵 ChromaLite: Neural Network-based Musical Scale Classifier
 
**ChromaLite** is a machine learning pipeline for predicting Western musical scales from audio using chromagrams. It includes a custom dataset generator, chroma feature extraction, and a simple neural network built with PyTorch.

> _Think of it as “Shazam for scale detection” — trained on music theory._

---

## 📁 Project Highlights

- 🔧 **Synthetic Dataset Generator**  
  Generates labeled chroma tensors for 24 Western scales using `music21`, `librosa`, and MIDI-to-audio synthesis.

- 🎼 **1,900+ Samples Across 24 Scales**  
  Each sample contains randomized notes in a specific scale, saved as chroma tensors and scale indices.

- 🧠 **Custom Neural Network Model (ChromaLite)**  
  A simple PyTorch-based neural network that learns to classify musical scales from `[1, 12, T]` chroma inputs.
---

## 🔬 Dataset Overview

- **Input:** Chroma tensor `[1, 12, T]` (12 pitch classes, variable time)
- **Output:** Integer scale index (0–23, covering major and minor scales)
- **Format:** `.pt` and `.csv` versions provided
- [👉 View Dataset on Kaggle](https://www.kaggle.com/datasets/omavashia/synthetic-scale-chromagraph-tensor-dataset)

---

## 🛠️ Tech Stack

- `Python`, `PyTorch`, `NumPy`, `pandas`  
- `music21`, `librosa`, `matplotlib`, `soundfile`, `FluidSynth`
---

## 📈 Results 

| Train Accuracy | Test Accuracy |
|----------------|---------------|
| 79.1%          | 78.28%         |

---

## 🔭 Future Work

- Add rhythmic diversity, chords, and velocity variation
- Generate more unique samples
- Build more models
