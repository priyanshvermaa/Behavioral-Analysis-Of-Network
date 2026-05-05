# Network Behavioral Analysis using Deep Learning

## Overview

This project focuses on **Network Behavioral Analysis** to detect malicious activities in network traffic using deep learning models.
It leverages flow-based network data and applies machine learning techniques to classify traffic as **benign or attack**.

The system uses:

* Autoencoder → for anomaly detection
* BiLSTM (Bidirectional LSTM) → for sequence-based classification

---

## Objectives

* Detect anomalies in network traffic
* Classify malicious vs normal behavior
* Compare performance of deep learning models
* Visualize attack patterns and probabilities

---

## Workflow

1. Dataset Preparation

   * Raw network flow data (CICIDS dataset)
   * Cleaning and merging multiple CSV files

2. Preprocessing

   * Feature selection
   * Normalization using scaler
   * Train-test split

3. Model Training

   * Autoencoder for anomaly detection
   * BiLSTM for sequence learning

4. Evaluation

   * Accuracy, confusion matrix, ROC curves
   * Comparison between models

5. Detection

   * Predict suspicious flows on unseen data

6. Visualization

   * Attack distribution
   * Probability graphs
   * Model comparison charts

---

## Project Structure

Network_Behavioral_Analysis/
│
├── data/                     # (Ignored in Git) Raw & processed datasets
│
├── models/                   # (Ignored in Git) Saved trained models
│
├── plots/                    # Visualization outputs (graphs, charts)
│
├── test_data/                # Test datasets & predictions
│
├── create_dataset.ipynb      # Dataset creation & merging
├── preprocess.ipynb          # Data preprocessing & scaling
├── train_autoencoder.ipynb   # Autoencoder model training
├── train_bilstm.ipynb        # BiLSTM model training
├── detect.ipynb              # Detection on new data
├── results.ipynb             # Model evaluation & comparison
├── visualize.ipynb           # Visualization of results
├── visualize_test.ipynb      # Test data visualization
├── test_dataset.ipynb        # Testing pipeline
│
├── requirements.txt          # Dependencies
├── .gitignore                # Ignored files
├── README.md                 # Project documentation
└── LICENSE

---

## Installation

```bash
git clone https://github.com/your-username/Behavioral_Analysis_Of_Network.git
cd Behavioral_Analysis_Of_Network
pip install -r requirements.txt
```

---

## How to Run

1. Run notebooks in order:

   * `create_dataset.ipynb`
   * `preprocess.ipynb`
   * `train_autoencoder.ipynb`
   * `train_bilstm.ipynb`
   * `results.ipynb`
   * `detect.ipynb`
   * `visualize.ipynb`

2. For testing:

   * `test_dataset.ipynb`
   * `visualize_test.ipynb`

---

## Models Used

### 🔹 Autoencoder

* Learns normal behavior
* Detects anomalies based on reconstruction error

### 🔹 BiLSTM

* Captures sequential dependencies
* Improves classification accuracy

---

## Results

* Compared Autoencoder vs BiLSTM performance
* Evaluated using:

  * Confusion Matrix
  * ROC Curve
  * Accuracy & Loss graphs

 BiLSTM generally performs better for sequence-based detection

---

## Dataset

* Based on **CICIDS Network Intrusion Dataset**
* Large files are not included in this repository
* You can download dataset from:

  * CICIDS official source or Kaggle

---

## Note

* Large files (datasets, models) are excluded using `.gitignore`
* Add your dataset in the `data/` folder before running

---

## Technologies Used

* Python
* Jupyter Notebook
* TensorFlow / Keras
* Scikit-learn
* Pandas, NumPy
* Matplotlib, Seaborn

---

## Author

Vaishnavi Kesarwani

---

## Future Improvements

* Real-time network traffic analysis
* Integration with intrusion detection systems
* Deployment as a web application
