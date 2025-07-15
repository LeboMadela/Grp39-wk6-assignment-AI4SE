# Grp39-wk6-assignment-AI4SE
# 🌐 AI Future Directions Assignment
**Theme:** *Pioneering Tomorrow’s AI Innovations*  
**Course:** AI for Software Engineering  
**Contributors:** Moleboheng Madela, Veronica Moshesha, Niniwe Xaka  

---

## 🔍 Overview

This collaborative project explores the future of Artificial Intelligence through emerging technologies, hands-on prototyping, and ethical discussions. The assignment spans:

- Theoretical analysis of Edge AI, Quantum AI, and Human-AI collaboration  
- A practical Edge AI prototype using TensorFlow Lite  
- Smart agriculture system design integrating AI-IoT  
- Ethical reflections on AI in personalized medicine  
- A 2030 futuristic AI proposal  
- (Bonus) Quantum computing simulation using IBM Qiskit

---

## 🧩 Assignment Structure

| Part | Description | Contributor |
|------|-------------|-------------|
| **Part 1** | Theoretical Analysis | Team Member 1 |
| **Part 2 - Task 1** | Edge AI Prototype (Waste Classification) | **You** |
| **Part 2 - Task 2** | AI-IoT Smart Farming System | Team Member 2 |
| **Part 2 - Task 3** | Ethics in Personalized Medicine | Team Member 3 |
| **Part 3** | AI 2030 Proposal | Team Member 1 |
| **Bonus** | Quantum AI Simulation | Team Member 2 |

---

## 🧠 Part 2 - Task 1: Edge AI Prototype (Your Contribution)

### 🎯 Objective

Develop a lightweight image classifier to recognize six types of garbage using a CNN model. Convert it to TensorFlow Lite for real-time, privacy-focused, on-device inference.

### 🗃️ Dataset

- **Name:** Garbage Classification Dataset  
- **Source:** [Kaggle](https://www.kaggle.com/datasets/mostafaabla/garbage-classification)  
- **Classes:** `plastic`, `paper`, `battery`, `glass`, `organic`, `metal`  
- **Total Samples:** ~4,650 (775 per class)

### 🏗️ Model Architecture

```plaintext
Input (150x150x3)
↓ Conv2D(16) + MaxPooling
↓ Conv2D(32) + MaxPooling
↓ Conv2D(64) + MaxPooling
↓ Flatten
↓ Dense(128) + Dropout(0.3)
↓ Dense(6, Softmax)
Loss: Categorical Crossentropy

Optimizer: Adam

Regularization: Dropout (0.3)

Augmentation: Flip, rotate, zoom, shift

📊 Training Metrics
Metric	Value
Final Training Accuracy	96%
Final Validation Accuracy	62%
Epochs	6 (EarlyStopping used)

✅ Results
Accuracy Metrics: Generated using classification_report()

Confusion Matrix: Available in report output

Overfitting Reduced: Using augmentation + dropout

Model Exported To: garbage_classifier_6classes.tflite

🧪 Real-Time Inference with TensorFlow Lite
python
Copy
Edit
Prediction: "Plastic" (Confidence: 0.87)
💡 Edge AI Benefits
Low latency — fast classification

Preserves privacy — data never leaves device

Saves bandwidth — no cloud dependency

Power-efficient — suitable for Raspberry Pi or smart bins

🚀 Project Setup
🔧 Requirements
bash
Copy
Edit
pip install tensorflow matplotlib pillow scikit-learn
🧑‍💻 How to Run (Colab)
Upload the dataset to your Google Drive.

Open the Colab notebook.

Mount your Google Drive.

Run all cells.

📦 Folder Structure
swift
Copy
Edit
/GarbageClassification/
├── battery/
├── glass/
├── metal/
├── organic/
├── paper/
└── plastic/
📁 Deliverables
File	Description
edge_ai_classifier.ipynb	Colab notebook with training + deployment
garbage_classifier_6classes.tflite	Exported TFLite model
report.pdf	Project analysis, accuracy metrics, deployment steps
README.md	Full documentation

📚 References
TensorFlow Docs: https://www.tensorflow.org

Kaggle Dataset: https://www.kaggle.com/datasets/mostafaabla/garbage-classification

PLP Academy Resources

IBM Quantum Experience: https://quantum-computing.ibm.com

🧠 Key Learning
This task provided hands-on experience with:

Building AI models that run on edge devices

Reducing model size for real-time use

Managing overfitting via augmentation and dropout

Converting models to TensorFlow Lite

Understanding ethical and practical implications of deploying AI at scale
