# Lung Disease Classification Using Transfer Learning with ResNet-18

This project focuses on classifying lung diseases (Normal, Lung Opacity, and Viral Pneumonia) using **ResNet-18** pre-trained on the **ImageNet** dataset. Transfer learning is leveraged to fine-tune the model for this specific medical image classification task. The dataset consists of medical images provided by **Fatemeh Mehrparvar** and is available on Kaggle under the **CC BY 4.0** license.

## Project Overview

The following techniques were used:
- **Transfer Learning**: Pre-trained ResNet-18 model is fine-tuned for the lung disease classification task.
- **Data Augmentation**: Random rotations, horizontal flips, and resized cropping were applied to improve model generalization.
- **Class Imbalance Handling**: Class weights were used in the loss function to address the imbalance between classes.
- **Early Stopping**: Training was stopped when the validation loss stopped improving to prevent overfitting.
- **Evaluation Metrics**: Precision, recall, F1-score, and confusion matrix were used to evaluate the model on the test set.

### GPU Used:
This model was trained using an **NVIDIA Tesla P100 GPU**, which significantly improved training time and allowed for more complex data augmentation and larger batch sizes.

## Dataset

The dataset used in this project consists of X-ray images categorized into three classes:
1. **Normal**
2. **Lung Opacity**
3. **Viral Pneumonia**

The dataset is provided by **Fatemeh Mehrparvar** and is available on Kaggle under the **CC BY 4.0** license. You can access the dataset [here](https://www.kaggle.com/datasets/fatemehmehrparvar/lung-disease).

### Dataset License:
This dataset is made available under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

### Dataset Splits:
- **Training set**: 70%
- **Validation set**: 15%
- **Test set**: 15%

## Model Performance

The model achieved an accuracy of **92%** on the test set, with strong precision, recall, and F1-scores across all classes. Here's a summary of the results:

- **Precision (weighted)**: 0.9235
- **Recall (weighted)**: 0.9215
- **F1-Score (weighted)**: 0.9218

### Class-wise Performance:
- **Normal**: Precision = 0.87, Recall = 0.93, F1-Score = 0.89
- **Lung Opacity**: Precision = 0.94, Recall = 0.89, F1-Score = 0.91
- **Viral Pneumonia**: Precision = 0.97, Recall = 0.95, F1-Score = 0.96

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/rachealakinboyo/lung-disease-classification.git
