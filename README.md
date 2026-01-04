# Detection of Deepfake Videos Using Long Distance Attention

## 🚀 Overview
This project focuses on detecting **AI-generated deepfake videos** using deep learning techniques.  
The model leverages **Long Distance Attention mechanisms** to capture global spatial–temporal dependencies across video frames, enabling robust detection of manipulated content.

Deepfake detection is a critical problem in media forensics, cybersecurity, and misinformation prevention.

---

## 🧠 Key Features
- Video-based deepfake detection (not just images)
- Spatial–temporal feature extraction from video frames
- Long Distance Attention to model global frame relationships
- End-to-end deep learning pipeline
- Proper evaluation using classification metrics

---

## 🏗️ System Architecture
1. Input deepfake / real videos  
2. Frame extraction & normalization  
3. CNN-based feature extraction  
4. Long Distance Attention layer  
5. Binary classification (Real vs Fake)

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Frameworks:** TensorFlow / Keras  
- **Computer Vision:** OpenCV  
- **Deep Learning:** CNN, Attention Mechanisms  
- **Tools:** NumPy, Pandas, Google Colab  

---

## 📂 Dataset
- Publicly available deepfake video datasets
- Videos converted into frame sequences for training
- Balanced real vs manipulated samples

*(Dataset details omitted intentionally for licensing reasons)*

---

## 📊 Model Evaluation
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix

The attention-based approach improves performance by capturing long-range dependencies across frames.

---

## ▶️ How to Run
```bash
pip install -r requirements.txt
python train.py
python evaluate.py
