# Pseudo-Labeling in Semi-Supervised Learning Using Fine-Tuned Binary Classifiers

## Project Summary

This project addresses the challenges of pseudo-labeling in semi-supervised learning. Traditional binary classifiers that use a one-vs-all approach suffer from significant drawbacks:
- **Class Imbalance**: Treating one class as positive and all others as negative leads to imbalanced data distributions.
- **Increased Computational Costs**: Training multiple binary classifiers independently increases training time and storage requirements.

To overcome these issues, this project introduces a novel approach:
- A **multi-class classifier** is trained and then fine-tuned to create binary classifiers.
- These binary classifiers are fine-tuned to predict pseudo-labels with higher accuracy, eliminating the need for oversampling or undersampling techniques.
- The predicted pseudo-labels are used to iteratively refine the multi-class classifier, achieving a balance between efficiency and performance.

The approach is validated using the MNIST and Fashion MNIST datasets to demonstrate its effectiveness in reducing computational overhead and improving label prediction accuracy.

---

## Repository Contents

### Folders
- **`content/labeled1`**: Contains all model files, including checkpoints and configurations for the multi-class and binary classifiers.
- **`data`**: Includes the datasets used for training and validation, specifically the MNIST and Fashion MNIST datasets.

### Files
- **`multiClassifier.ipynb`**: A Jupyter Notebook containing the complete code implementation for:
  1. Training the initial multi-class classifier.
  2. Creating and fine-tuning binary classifiers for pseudo-label prediction.
  3. Iteratively refining the multi-class classifier using pseudo-labeled data.
  
---

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Deepikach025/Project_Classification.git


## Results

### The proposed approach demonstrates:

- Improved pseudo-label prediction accuracy compared to traditional binary classifiers.
- Reduced training time and computational costs by avoiding oversampling or undersampling.
- Validation on the MNIST and Fashion MNIST datasets showcases the approach's generalizability and robustness.
