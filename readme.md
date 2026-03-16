# 🍔 Food-11 Image Classification: Transfer Learning Excellence

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![MLflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=for-the-badge&logo=mlflow&logoColor=blue)
![DagsHub](https://img.shields.io/badge/DagsHub-000000?style=for-the-badge&logo=dagshub&logoColor=white)
![EfficientNet](https://img.shields.io/badge/EfficientNet-B0-green?style=for-the-badge)

## 🎯 Overview
This project leverages **Transfer Learning** to classify images into 11 food categories using the **EfficientNetB0** architecture. By utilizing advanced MLOps tools like **MLflow**, we tracked every experiment to ensure the highest accuracy and best generalization.

---

## 🛠️ Tech Stack & MLOps
| Category | Technology |
| :--- | :--- |
| **Model Architecture** | EfficientNetB0 (ImageNet Weights) |
| **Environment** | Google Colab (GPU Accelerated) |
| **Tracking & Logging** | MLflow + DagsHub |
| **Optimization** | Adam + ReduceLROnPlateau |
| **Regularization** | EarlyStopping + Dropout (0.3) |

---

## 🧪 Experiments Dashboard

### 🔹 Experiment 1: Feature Extraction
* **Strategy:** Froze all base layers; trained only the custom classification head.
* **Epochs:** 10 (Stopped early by Callback).
* **Accuracy:** ~96% (Validation).
* **Observation:** Established a very strong baseline with minimal training time.

### 🔹 Experiment 2: Fine-Tuning
* **Strategy:** Unfroze the **top 20 layers** with a Learning Rate of $10^{-5}$.
* **Result:** Pushed Validation Accuracy to **~97.5%**.
* **Observation:** The model adapted perfectly to food-specific textures and patterns.

---

## 📈 Key Insights & Observations

> [!IMPORTANT]
> **1. Convergence:** The model reached peak performance quickly due to the pre-trained power of EfficientNet.
> 
> **2. Generalization:** High Validation Accuracy (97%+) compared to Training Accuracy indicates excellent generalization and no significant overfitting.
> 
> **3. EarlyStopping:** Successfully prevented unnecessary training, saving time and preserving model weights at their best performance.

---

## 🧬 Bonus: MLflow Tracking
We integrated **MLflow** with **DagsHub** to maintain a versioned history of:
* **Parameters:** Learning Rate, Batch Size, Trainable Layers.
* **Metrics:** Accuracy and Loss curves.
* **Artifacts:** The final trained model weights (`.h5`).

---

## 📊 Visualizations
### Training History (Feature Extraction vs Fine-Tuning)

<img width="565" height="435" alt="image" src="https://github.com/user-attachments/assets/51186777-3460-47ce-8ac8-89aa01a9af32"/>


 <img width="556" height="435" alt="image" src="https://github.com/user-attachments/assets/7f7e4c90-c254-4d28-84cc-7202387b6820" />
 

---

## 🔗 Live Experiment Tracking
You can access the full interactive dashboard for this project's experiments on **DagsHub** via the following link:
👉 [Click here to view MLflow Dashboard](https://dagshub.com/Aside00/Food11-EfficientNet.mlflow/#/experiments/0/runs)

### What you will find there:
* **Run Comparisons:** Side-by-side metrics for Feature Extraction and Fine-tuning.
* **Hyperparameter Logs:** Details on learning rates, batch sizes, and callbacks.
* **Interactive Graphs:** Dynamic charts showing accuracy/loss progression over time.
---
