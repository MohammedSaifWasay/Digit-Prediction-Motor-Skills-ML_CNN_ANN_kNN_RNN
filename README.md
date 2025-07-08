# ✍️ Predicting Handwritten Digits to Identify Motor Skill Deficiencies

## 🧠 Overview
This project explores the application of machine learning models to predict handwritten digits and analyze their potential to identify motor skill deficiencies in students. Using a pixel-based dataset (`letters.csv`), we compare the performance of four classification algorithms—**K-Nearest Neighbors (KNN)**, **Artificial Neural Networks (ANN)**, **Convolutional Neural Networks (CNN)**, and **Recurrent Neural Networks (RNN)**—to evaluate their effectiveness in image recognition and diagnostic support.

---

## 🎯 Objectives

- Classify handwritten digits (0–9) from image pixel data.
- Compare ML and DL models based on classification accuracy and learning performance.
- Explore the potential of using misclassifications to identify motor skill deficiencies in students.

---

## 📦 Dataset

- **Name**: `letters.csv`
- **Size**: Each row represents an image (flattened pixel values).
- **Target Variable**: Digit label (0–9)
- **Features**: Pixel intensities of handwritten characters

---

## 🧪 Methodology

### 🔍 Preprocessing

- Data loading and inspection using `pandas`.
- Train-test split (80:20)
- Normalization of pixel values (scaled to [0,1]).
- One-hot encoding of labels for multi-class classification.

### 🤖 Model Implementations

| Model | Description | Architecture | Test Accuracy |
|-------|-------------|--------------|---------------|
| **KNN** | Baseline model based on proximity | k=3 neighbors | 62% |
| **ANN** | Feedforward neural network | 1 hidden layer (128 units) + dropout | 68% |
| **CNN** | Convolutional network for spatial features | 2 conv + pooling → dense | **71%** |
| **RNN (LSTM)** | Sequence modeling for spatial sequences | 2 LSTM layers → dense | 70% |

---

## 📈 Evaluation Metrics

- **Accuracy**
- **F1 Score**
- **Confusion Matrix**
- **Training/Validation Loss & Accuracy Plots**

---

## 📊 Results Summary

### ✅ CNN
- Highest test accuracy (71%)
- Best spatial feature extraction
- Fewer misclassifications across all digits

### ✅ RNN
- Competitive with CNN (70%)
- Effective at capturing sequential patterns in stroke data

### ⚠️ KNN & ANN
- Lower accuracy (62–68%)
- Higher misclassification rates

---

## 💡 Insights & Implications

- Misclassifications—especially frequent errors like misreading 3s and 5s—could reflect **fine motor skill deficiencies**.
- Consistent digit confusion may suggest **cognitive or coordination issues**, making these models useful for early diagnosis and intervention.
- CNN and RNN models show the **highest potential** for practical deployment in educational or clinical settings.

---

## 🛠 Tools & Libraries

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib, Seaborn

---

## 🔮 Future Work

- Add handwriting trajectory/time-series data for better RNN modeling.
- Integrate clinical annotations on motor skill deficiencies.
- Test transfer learning using pretrained CNN models (e.g., ResNet, MobileNet).
- Improve generalization using regularization and augmentation.

---

## 📚 References

- LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep Learning. *Nature, 521(7553)*, 436–444.
- Graves, A. (2013). *Supervised Sequence Labelling with Recurrent Neural Networks*. Springer.
- Piek, J. P., et al. (2007). Motor Coordination and Social Emotional Problems. *Dev. Medicine & Child Neurology*.
- King, R. D., & Zeng, H. (2020). Evaluation Metrics for ML Classification. *JMLR*.
- Little, R. J. A., & Rubin, D. B. (2019). *Statistical Analysis with Missing Data*.

---

## 🧠 Author  
**Mohammed Saif Wasay**  
*Data Analytics Graduate — Northeastern University*  
*Machine Learning Enthusiast | Passionate about turning data into insights*  

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/mohammed-saif-wasay-4b3b64199/)

---
