# Arabic Broken Plural RNN

This repository demonstrates the use of Recurrent Neural Networks (RNN) to predict the **plural forms of Arabic singular words**. The model is implemented using **Keras** and leverages deep learning techniques to analyze Arabic morphology, focusing on the distinction between **broken plurals** and **sound plurals**.

## Table of Contents

- [Overview](#overview)
- [Dataset Structure](#dataset-structure)
- [Implementation Details](#implementation-details)
  - [Libraries Used](#libraries-used)
  - [Helper Functions](#helper-functions)
  - [Model Architecture](#model-architecture)
- [Results](#results)

## Overview

Arabic plurals can be categorized into:

1. **Sound Plurals**: Regular patterns for forming plurals.
2. **Broken Plurals**: Irregular patterns that modify the structure of the singular form.

This project applies RNNs to predict plural forms by learning the transformations between singular and plural patterns in Arabic. The model also incorporates **linguistic features** like lemma, root, and morphological patterns for better prediction accuracy.

## Dataset Structure

The dataset is organized into CSV files for training (`train_pairs_all.csv`), validation (`dev_pairs_all.csv`), and testing (`test_pairs_all.csv`). Each row represents a word pair and includes linguistic features.

### Key Columns:

- **lemma**: Singular form of the word.
- **inflection**: Plural form of the lemma.
- **NUM**: Number (e.g., Singular/Plural).
- **GEN**: Gender (e.g., Masculine/Feminine).
- **RAT**: Rationality (Rational/Irrational).
- **lex_freq**: Lexical frequency of the word.
- **B/S**: Indicates if the plural is Broken (B) or Sound (S).
- **SING_PATT**: Singular morphological pattern.
- **PL_PATT**: Plural morphological pattern.
- **ROOT**: Root morpheme of the word.
- **FREQ**: Frequency of occurrence in the dataset.

## Implementation Details

### Libraries Used

The following libraries are utilized in the project:

- **TensorFlow/Keras**: For building and training the RNN model.
- **Hugging Face Transformers**: To preprocess Arabic text using the Arabic BERT tokenizer.
- **scikit-learn**: For data preprocessing, model evaluation, and error analysis.
- **Pandas**: For data handling and manipulation.
- **Matplotlib**: For visualizing results.

### Helper Functions

The code includes a variety of helper functions to:

- Preprocess the dataset (e.g., encoding Arabic text and handling duplicates).
- Map between Arabic script and Buckwalter transliteration.
- Perform error analysis (e.g., generating reports on misclassifications).
- Evaluate the model using metrics like confusion matrices and classification reports.

### Model Architecture

The model uses an RNN-based architecture with layers like:

- **LSTM**: For capturing long-term dependencies in Arabic morphological structures.
- **Dense Layers**: For transforming RNN outputs into predictions.
- **Dropout**: For regularization to avoid overfitting.

## Results

The model's performance is evaluated based on:

- **Accuracy**: Percentage of correct predictions.
- **Loss**: Measures the model's error during training and testing.
- **Precision, Recall, and F1-Score**: Detailed classification metrics for Broken and Sound plurals.
