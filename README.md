# 🎭 Deepfake Detection Using Hybrid Multi-Modal Synthetic-to-Real Image Mapping

## 📘 Project Overview

This project proposes a novel and interpretable pipeline for deepfake detection by combining texture analysis, motion tracking, and physiological coherence in facial and non-facial regions. With the rise of highly photorealistic synthetic videos generated using GANs and neural face rendering, traditional detection methods often fall short in detecting subtle forgeries.

Our pipeline introduces a **multi-branch architecture** that not only analyzes pixel-level texture artifacts using **EfficientNet-B4**, but also captures **micro-muscle movements** through **optical flow estimation**, evaluates **facial symmetry**, and computes a novel **Neuro-Muscular Coherence Score (NMCS)** to understand the authenticity of expressions and facial dynamics. The goal is not just to detect, but to **explain**—highlighting manipulated zones and inconsistencies in motion.

---

## 🧠 Key Features

- 🧩 **Multi-Branch Deepfake Detection Pipeline**  
- 🎯 **Zone-Wise Texture Artifact Detection** using EfficientNet-B4  
- 🎥 **Micro-Muscle Optical Flow Estimation** with motion heatmaps  
- ⚖️ **Facial Symmetry & Expression Analysis** (e.g., blink balance, cheek lift)  
- 🧠 **Neuro-Muscular Coherence Score (NMCS)** for physiological consistency  
- 📊 **Explainable Predictions** with region-based inconsistency maps  
- 📁 **Modular Training** and easy integration of custom datasets  

---

## 🔧 Technologies & Tools

| Tool / Library              | Purpose                                                   |
|----------------------------|-----------------------------------------------------------|
| 🐍 Python 3.8+              | Core development language                                 |
| 🔥 PyTorch                  | Deep learning framework                                   |
| 🧠 EfficientNet-B4          | Feature extraction and texture analysis                   |
| 🎯 MediaPipe                | Face detection and landmark tracking                      |
| 🎞️ Optical Flow (Farneback) | Temporal motion tracking and micro-expression estimation  |
| 📊 Matplotlib / Seaborn     | Plotting and performance visualization                    |
| 🧪 pandas / PIL / OpenCV    | Data handling and image I/O                               |

---
## 🛠️ Architecture

The detection pipeline consists of the following stages:

1. **Face Detection & Alignment** (via MediaPipe)
2. **Facial Zone Segmentation**
3. **Multi-Branch Feature Extraction:**
   - EfficientNet-based Texture Analysis
   - Optical Flow for Micro-Movements
   - NMCS computation for physiological coherence
4. **Feature Fusion**
5. **Classification Head** (Transformer)
6. **Output:** Probability Score + Explanation Map

---

## 🧪 How It Works

1. **Input**: Short video clip or sequence of facial frames  
2. **Face Detection & Alignment**: Facial zones segmented using landmarks  
3. **Feature Extraction**: Parallel branches extract texture, motion, symmetry, and tension  
4. **NMCS Computation**: Measures coordination across facial zones  
5. **Fusion + Classification**: All features concatenated and passed through a classifier  
6. **Output**: Real / Fake prediction with explanation map  

---

## 📈 Results

- ✅ **Accuracy**: Achieved up to **93% accuracy** on Celeb-DF frame-level validation  
- 🧠 High interpretability with visual anomaly maps  
- 🔍 Strong generalization across both facial and non-facial forgery zones  

---

## 🌐 Real-World Applications

- 📰 **Media Integrity Verification**  
- 👮 **Digital Forensics**  
- 📹 **Social Media Content Moderation**  
- 🧪 **AI Model Evaluation and Research**  

---

## 🚀 Future Scope

- Integration of audio-lip sync mismatch analysis  
- Lightweight version for edge deployment (e.g., mobile forensic tools)  
- Adversarial robustness and domain adaptation across datasets  
