# **Intrusion Detection System - Machine Learning Project (2024/25) - Tor Vergata**

This repository contains the implementation of an **Intrusion Detection System (IDS)** using Machine Learning models, based on the **NSL-KDD** dataset. The project was developed as part of the **Machine Learning Course 2024/25**, focusing on supervised classification techniques to detect and classify network intrusions.

---

## **Project Description**
### **Track: T7b**
The project is based on the following track description:

> The **NSL-KDD dataset** represents a benchmark for intrusion detection systems. The dataset contains information about network traffic flows to an IT infrastructure. Each flow is labeled as either "normal" or associated with a type of attack. The `label` column in the dataset represents the classification label.
>
> The task requires training Machine Learning models for the following goals:
> 1. **Binary classification** of flows as "normal" or "attack".
> 2. **Multiclass classification** to recognize the specific type of attack.

---

## **Dataset**
The project uses the **NSL-KDD dataset**, a well-known benchmark for evaluating intrusion detection systems. Key characteristics of the dataset:
- Contains labeled network traffic flows.
- Includes both normal and attack data, with several attack categories.
- Preprocessed to remove duplicate and redundant records.

---

## **Goals**
The main objectives of this project are:
1. Develop and train machine learning models for intrusion detection.
2. Perform binary classification (normal vs. attack) and multiclass classification (specific attack types).
3. Optimize model performance through preprocessing and hyperparameter tuning.
4. Visualize and analyze the results to gain insights into model behavior.

---

## **Models and Methods**
The following models and methods were implemented:
1. **Random Forest**:
   - Used for its robustness and interpretability.
   - Hyperparameters were tuned using random search.
2. **Multi-Layer Perceptron (MLP)**:
   - Implemented using TensorFlow/Keras.
   - Optimized with Keras Tuner to find the best architecture and hyperparameters.

### **Preprocessing**
- **Handling Correlations**: Highly correlated features (correlation > 0.8) were removed.
- **Balancing Classes**: The maximum number of samples per class was limited to the average of the cardinality of each class with a maximum of 3600 samples to overcome the imbalance between classes.
- **Encoding**: Categorical features were encoded using label encoding.

---

## **Results**
- Models were evaluated using:
  - **Accuracy**
  - **F1-Score (Macro)**
  - **Cross-Validation** (for MLP)
- The **Random Forest** model performed consistently well across all tasks.
- The **MLP** model demonstrated the ability to capture complex patterns in the data.

---

## **How to Run**
1. Open the notebook in Jupyter or Google Colab:
   - [Intrusion Detection Notebook](https://colab.research.google.com/drive/1OaQxuGDRj2H6Smj5XZ6tRKWJnP-oI5jl?usp=sharing)
4. Run all cells to preprocess the dataset, train models, and evaluate performance.
