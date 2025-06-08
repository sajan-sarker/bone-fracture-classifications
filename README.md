# 🦴 Bone Fracture Classification Using Deep Learning

### CSE465 - Pattern Recognition and Neural Network Course Project Content

## 🧠 About the Project
This project presents a deep learning approach for classifying **bone X-ray images** into two categories: **Fractured** and **Not Fractured**, using **Transfer Learning**.
The primary goal is to assist medical professionals by providing a reliable second opinion to detect bone fractures accurately and efficiently. By leveraging **image-based classification techniques**, the model learns visual patterns associated with fractures, helping to improve diagnostic speed and accuracy.
To achieve robust results, the project utilizes two well-established pre-trained models:

- **EfficientNet**
- **VGG16**

Both models were fine-tuned on a labeled medical X-ray dataset, and their performance was evaluated using standard classification metrics.

## 🧠 Models Used
### ✅ EfficientNet (B0)
- Parameters: 4.01M
- Accuracy: 99.21%
- No of Epochs: 50
- Training Time: ~57 minutes
- Avgerage Epoch Time: ~1.5 mins
- Environment: Kaggle, P100 GPU

### ✅ VGG16
- Parameters: 134.27M
- Accuracy: 98.42%
- No of Epochs: 50
- Training Time: ~1.5 hours
- Avgerage Epoch Time: ~3.5 mins
- Environment: Kaggle, P100 GPU

## 🔬 Dataset
- Medical X-ray images categorized into Fractured and Not Fractured
- Used for supervised learning classification
- Dataset Source: [Kaggle Bone Fracture Dataset](https://www.kaggle.com/datasets/bmadushanirodrigo/fracture-multi-region-x-ray-data) 

## ⚙️ Training Configuration

- **Loss Function:** Cross Entropy Loss  
- **Optimizer:** Stochastic Gradient Descent (SGD)  
  - Learning Rate: 0.001  
  - Momentum: 0.9  
  - Weight Decay: 1e-4  
- **Scheduler:** ReduceLROnPlateau  
  - Mode: `min` (based on validation loss)  
  - Factor: 0.1  
  - Patience: 5

## 📊 Performance Metrics

### 🔍 Classification Report (EfficientNet)

| Class          | Precision | Recall | F1-score | Support |
|----------------|-----------|--------|----------|---------|
| Fractured      | 1.00      | 0.98   | 0.99     | 238     |
| Not Fractured  | 0.99      | 1.00   | 0.99     | 268     |
| **Accuracy**   |           |        | **0.99** | 506     |


### Visual Results (Learning Curve)
<img src="https://github.com/sajan-sarker/bone-fracture-classifications/blob/main/eff_learning_curve.png?raw=true" alt="Learning Curve" width="500"/>
