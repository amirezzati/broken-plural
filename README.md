# Arabic Broken Plural RNN

This repository demonstrates the use of Recurrent Neural Networks (RNN) to predict the **plural forms of Arabic singular words**. The model is implemented using **Keras** and leverages deep learning techniques to analyze Arabic morphology, focusing on the distinction between **broken plurals** and **sound plurals**.

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
