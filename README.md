# 🎵 ChromaLite: Convolutional Neural Network-based Musical Scale Classifier
 
**ChromaLite** is a deep learning pipeline for predicting Western musical scales from audio using chromagrams. It includes a custom dataset generator, chroma feature extraction, and a lightweight convolutional neural network (CNN) built with PyTorch.

> _Think of it as “Shazam for scale detection” — trained on music theory._

---

## 📁 Project Highlights

- 🔧 **Synthetic Dataset Generator**  
  Generates labeled chroma tensors for 24 Western scales using `music21`, `librosa`, and MIDI-to-audio synthesis.

- 🎼 **7,200+ Samples Across 24 Scales**  
  Each sample contains randomized notes in a specific scale, saved as chroma tensors and scale indices.

- 🧠 **Custom CNN Model (ChromaLite)**  
  A lightweight PyTorch-based CNN that learns to classify musical scales from `[1, 12, T]` chroma inputs.

- 🔁 **Currently Improving Generalization**  
  Exploring dataset enhancements with rhythmic variation, rests, polyphony, and mixed octaves.

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

## 📈 Results (⚠️ Currently investigating overfitting — next steps include improving dataset realism.)

| Epoch | Train Accuracy | Test Accuracy |
|-------|----------------|---------------|
| 8     | 97.2%          | 81.39%         |

- Also need to address randomization in `Scales()` dataset generator class
---

## 🔭 Future Work

- Add rhythmic diversity, chords, and velocity variation
- Train on polyphonic samples
