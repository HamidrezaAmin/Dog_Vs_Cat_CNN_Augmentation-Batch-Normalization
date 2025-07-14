
# 🐶 Dogs vs. Cats Image Classifier with Batch Normalization and Augmentation

This project implements a Convolutional Neural Network (CNN) using Keras to classify images of dogs and cats. 
We explored various techniques such as **Dropout**, **Data Augmentation**, and **Batch Normalization** to improve model generalization and reduce overfitting.

---

## 📌 Project Overview

- **Dataset**: Kaggle Dogs vs. Cats
- **Framework**: TensorFlow / Keras
- **Image Size**: 150x150
- **Model Type**: Sequential CNN

---

## ⚙️ Key Features

### ✅ Dropout
- Used to randomly deactivate 50% of neurons to prevent overfitting.
- Helps the model generalize better by not becoming too reliant on any one feature.

### ✅ Data Augmentation
- Introduces new variations of existing images through:
  - Rotation, Zoom, Width/Height Shift, Shear, Flip
- Allows the model to see more diverse inputs during training without needing more data.

### ✅ Batch Normalization
- Added after each convolutional layer (after ReLU) to:
  - Normalize the output of layers
  - Speed up convergence
  - Make the model more stable during training
- For ReLU, **BN is typically applied after the activation**.

---

## 📊 Performance Summary

| Configuration                   | Training Accuracy | Validation Accuracy |
|----------------------------------|-------------------|---------------------|
| With Dropout Only                | 99.37%            | 77.85%              |
| With Augmentation Only           | 81.03%            | 81.80%              |
| With BatchNorm + Augmentation    | 84.04%            | 81.40%              |

> 🧠 Note: While Dropout achieved high training accuracy, it overfit the training data. Augmentation and BatchNorm yielded a more generalizable model.

---

## 📁 Project Structure

```
base_dir/
├── train/
│   ├── cat/
│   └── dog/
├── validation/
│   ├── cat/
│   └── dog/
└── test/
```

---

## 🚀 How to Run

1. Upload the dataset to your `base_dir` in Google Colab or local environment.
2. Train the model using the `model.fit()` function.
3. Evaluate results with and without augmentation and BatchNorm.
4. Compare validation accuracy and adjust parameters as needed.

---

## 📌 Conclusion

Using **Data Augmentation + Batch Normalization** offers a strong regularization strategy, helping the model achieve better generalization and outperform Dropout-only networks.
