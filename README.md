# Eye Disease Classification and Severity Grading using EfficientNet and Graph Convolutional Networks

## 📌 Project Overview
This project presents an AI-based pipeline for **automated diagnosis of eye diseases** from fundus images.  
The system leverages **EfficientNet** for powerful image feature extraction and **Graph Convolutional Networks (GCN)** for relational reasoning between features.  
It classifies fundus images into four categories:  

- Diabetic Retinopathy  
- Cataract  
- Glaucoma  
- Normal  

In addition, a **severity grading module** was developed to provide finer disease progression insights, which is critical for clinical decision support.  

---

## 🛠️ Methodology

### 🔹 Preprocessing
- Grayscale conversion  
- Contrast enhancement  
- Channel-wise wavelet decomposition (LL, HL, LH, HH bands)  
- Image resizing to 224×224  
- Conditional preprocessing applied only if not already enhanced  

### 🔹 Model Architecture
- **EfficientNetB0**  
  - Pretrained on ImageNet, used with `include_top=False`  
  - Extracts deep embeddings from preprocessed fundus images  

- **Graph Convolutional Network (GCN)**  
  - Converts EfficientNet embeddings into nodes  
  - Defines edges using spatial and statistical similarities  
  - Processes the graph to refine disease classification  

- **Graph Coarsening & Refining**  
  - **Graph Coarsening:** Merges redundant or highly similar nodes, capturing global structural patterns while reducing complexity  
  - **Graph Refining:** Gradually restores fine-grained details, improving local feature representation and classification robustness  

### 🔹 Severity Grading
- Researched **clinical biomarkers** and risk factors for each disease  
- Designed an algorithm that integrates **clinical indicators** with **image-based embeddings**  
- Automatically quantifies severity levels (e.g., mild, moderate, severe) for each case  

---

## 🎯 Key Outcomes
- Achieved **high accuracy** in 4-class classification  
- Enhanced disease representation through **hybrid CNN+GCN modeling**  
- Introduced **hierarchical graph processing (coarsening/refining)** for improved interpretability and robustness  
- Developed an **automatic severity grading system** to support early detection and clinical decision-making  

---

## 🚀 Tech Stack
- Python  
- TensorFlow / PyTorch  
- OpenCV, NumPy, Pandas  
- Matplotlib, Seaborn for visualization  

---

## 📖 Future Work
- Expand dataset with more diverse clinical fundus images  
- Integrate **explainable AI (XAI)** for better interpretability in medical diagnosis  
- Deploy as a **web-based screening tool** for ophthalmologists  

---
