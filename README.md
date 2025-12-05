# Audio Command Recognition Using MFCC Features and SVM

### Master's Program -- Computer Science

**Faculty of Science, Alexandria University**\
**Course:** Pattern Recognition

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF)
![License](https://img.shields.io/badge/License-MIT-green)
![Accuracy](https://img.shields.io/badge/Accuracy-92.42%25-brightgreen)

------------------------------------------------------------------------

This project implements a lightweight and efficient speech command
recognition system capable of classifying two spoken commands: **"yes"**
and **"no"**. The system uses **Mel-Frequency Cepstral Coefficients
(MFCCs)** for feature extraction and a **Support Vector Machine (SVM)**
classifier for prediction.

The project demonstrates how classical machine learning techniques can
achieve strong performance on limited-vocabulary speech recognition
tasks without relying on deep learning.

------------------------------------------------------------------------

## 📁 Project Structure

``` text
├── Audio_Command_Recognition_MFCC_SVM_Report.pdf
├── Audio_Command_Recognition_MFCC_SVM_Notebook.ipynb
├── test_data/
│   ├── test_no.wav
│   └── test_yes.wav
└── figures/
    ├── confusion_matrix.png
    └── roc_curve.png
```

------------------------------------------------------------------------

## 📄 Files Description

  ---------------------------------------------------------------------------------
  File / Folder                                     Description
  ------------------------------------------------- -------------------------------
  `Audio_Command_Recognition_MFCC_SVM_Report.pdf`   Full scientific project report
                                                    containing methodology,
                                                    experiments, and results

  `Audio_Command_Recognition_MFCC_SVM_Notebook.ipynb`      Jupyter Notebook containing the
                                                    complete implementation

  `test_data/`                                      Sample WAV audio files for
                                                    real-time inference testing

  `figures/`                                        Generated evaluation plots
                                                    (confusion matrix and ROC
                                                    curve)
  ---------------------------------------------------------------------------------

------------------------------------------------------------------------

## 🎯 Project Objective

To build a **simple, fast, and interpretable speech command recognition
system** that can: - Extract discriminative MFCC features from audio, -
Train a linear SVM classifier, - Accurately distinguish between
**"yes"** and **"no"** spoken commands, - Support **real-time
inference** for new audio samples.

------------------------------------------------------------------------

## 📊 Dataset

-   Based on the **Google Speech Commands Dataset (v0.02)**
-   Two selected classes:
    -   `"yes"`
    -   `"no"`
-   Final dataset split:
    -   **Training samples:** 6,388
    -   **Testing samples:** 1,597
-   Feature dimension:
    -   **26 features per sample** (13 MFCC means + 13 MFCC standard
        deviations)

------------------------------------------------------------------------

## ⚙️ Methodology

### 1. Audio Preprocessing

-   Resampling to **16 kHz**
-   Fixed duration: **1.0 second**
-   Zero-padding or trimming
-   Optional normalization

### 2. Feature Extraction

-   **13 MFCC coefficients per frame**
-   Time-wise statistical aggregation:
    -   Mean
    -   Standard deviation
-   Final feature vector size: **26**

### 3. Classification

-   **Support Vector Machine (SVM)**
-   Kernel: **Linear**
-   Feature scaling: **StandardScaler**
-   Probability estimation enabled for ROC/AUC

------------------------------------------------------------------------

## ✅ Final Results

  Metric          Value
  --------------- ------------
  **Accuracy**    **92.42%**
  **AUC Score**   **0.9778**

### Detailed Test Set Performance

  Class   Precision   Recall   F1-score   Samples
  ------- ----------- -------- ---------- ---------
  no      0.92        0.93     0.92       788
  yes     0.93        0.92     0.92       809

------------------------------------------------------------------------

## 📈 Evaluation Visualizations

-   ✅ Confusion Matrix → `figures/confusion_matrix.png`
-   ✅ ROC Curve → `figures/roc_curve.png`

------------------------------------------------------------------------

## 🎙️ Real-Time Inference

The notebook allows you to test the trained model on new audio files.

### Example Prediction Output:

``` text
File: test_yes.wav
Prediction: yes
Probabilities:
  no: 0.0705
  yes: 0.9295
```

------------------------------------------------------------------------

## 🛠️ Tools & Libraries Used

-   Python 3.11
-   NumPy
-   Librosa
-   Scikit-learn
-   Matplotlib
-   Jupyter Notebook

------------------------------------------------------------------------

## 🔗 Kaggle Notebook

You can access and run the full project directly on Kaggle using the
following link:

**https://www.kaggle.com/code/fareshazem/yes-no-speech-command-classification**

------------------------------------------------------------------------

## 🚀 How to Run the Project Locally

1.  Open the notebook:

    ``` bash
    jupyter notebook yes_no_speech_command_classification.ipynb
    ```

2.  Run all cells to:

    -   Load audio data
    -   Extract MFCC features
    -   Train the SVM model
    -   Evaluate performance
    -   Test real-time predictions

3.  Place any test WAV file inside:

        test_data/

------------------------------------------------------------------------

## 📌 Key Features

-   Lightweight classical ML pipeline
-   High accuracy with low computational cost
-   Easily deployable for embedded/edge devices
-   Fully interpretable model
-   Real-time inference capability

------------------------------------------------------------------------

## 👨‍💻 Author

**Fares Hazem**\
Master's Student -- Computer Science\
Faculty of Science, Alexandria University\
Course: Pattern Recognition

------------------------------------------------------------------------

## 📚 References

-   Warden, P. (2018). *Speech Commands: A Dataset for
    Limited-Vocabulary Speech Recognition.*
-   Jurafsky & Martin (2021). *Speech and Language Processing.*
-   Librosa Documentation: https://librosa.org
-   Scikit-learn Documentation: https://scikit-learn.org
