# TabMJDroid
# TabMJDroid: An Interpretable Stacking-Based Ensemble Framework for Android Malware Detection

## Overview

TabMJDroid is a hybrid Android malware detection framework that combines **TabNet** and **LightGBM** using a **Logistic Regression** meta-classifier within a stacking ensemble architecture. The framework is designed to improve malware detection accuracy while maintaining model interpretability and scalability for large Android malware datasets.

The implementation accompanies the research paper:

**"TabMJDroid: An Interpretable Stacking-Based Ensemble Framework for Android Malware Detection"**

---

## Project Structure

```
TabMJDroid/
│
├── README.md
├── requirements.txt
├── hyperparameters.txt
├── TabMJDroid.ipynb
│
├── data/
│   ├── train_data.csv
│   ├── validation_data.csv
│   └── test_data.csv
│
└── results/
```

---



## Dataset

The proposed framework was evaluated using the following publicly available Android malware datasets:

### 1. MH-100K Dataset

* Purpose: Large-scale Android malware detection
* Samples: 101,934 Android applications
* Benign Applications: 92,134
* Malware Applications: 9,800

### 2. CICInvesAndMal2019 Dataset

* Purpose: Benchmark dataset for Android malware detection
* Used for comparative evaluation of the proposed framework.

Note: Due to dataset licensing and distribution policies, the datasets are not included in this repository. 
Please obtain them from their respective official sources before running the experiments.


---

## Experimental Configuration

* Training Set: 70%
* Validation Set: 15%
* Test Set: 15%
* Data Split: Stratified Sampling
* Random Seed: 42

---

## Model Architecture

The proposed framework consists of the following stages:

1. Data preprocessing
2. Feature normalization and label encoding
3. Training the TabNet classifier
4. Training the LightGBM classifier
5. Generation of probability predictions
6. Concatenation of prediction probabilities
7. Training the Logistic Regression meta-classifier
8. Final malware classification
9. Performance evaluation

---

## Hyperparameters

The complete hyperparameter configuration is provided in the file:

```
hyperparameters.txt
```

---

## Software Requirements

* Python 3.x
* PyTorch
* pytorch-tabnet
* LightGBM
* scikit-learn
* NumPy
* Pandas
* Matplotlib

Install the required packages using:

```
pip install -r requirements.txt
```

---

## Running the Project

1. Download the required datasets.
2. Place the datasets in the appropriate data directory.
3. Open `TabMJDroid.ipynb` in Google Colab or Jupyter Notebook.
4. Execute the notebook. 
5. The notebook performs preprocessing, model training, validation, testing, and evaluation.

---

## Performance Metrics

The framework reports:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC

---

## Reproducibility

To ensure reproducibility:

* A fixed random seed of 42 was used.
* Stratified train-validation-test splitting was employed.
* All hyperparameters are documented in `hyperparameters.txt`.

---

## Citation

If you use this implementation in your research, please cite the corresponding publication.

---

## Contact

For questions regarding the implementation, please contact the corresponding author.

