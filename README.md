````markdown
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
- [How to Run the Code](#how-to-run-the-code)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Arabic plurals can be categorized into:

1. **Sound Plurals**: Regular patterns for forming plurals.
2. **Broken Plurals**: Irregular patterns that modify the structure of the singular form.

This project applies RNNs to predict plural forms by learning the transformations between singular and plural patterns in Arabic. The model also incorporates **linguistic features** like lemma, root, and morphological patterns for better prediction accuracy.

---

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

---

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

---

## Results

The model's performance is evaluated based on:

- **Accuracy**: Percentage of correct predictions.
- **Loss**: Measures the model's error during training and testing.
- **Precision, Recall, and F1-Score**: Detailed classification metrics for Broken and Sound plurals.

### Error Analysis

Comprehensive reports highlight:

- Common misclassifications.
- Analysis of unseen errors (e.g., words with patterns not present in the training set).
- Distinctions between broken and sound plural errors.

---

## How to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/itsfaryar/Arabic-Broken-Plural-RNN.git
   cd Arabic-Broken-Plural-RNN
   ```
````

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter Notebook:

   ```bash
   jupyter notebook Arabic_broken_plurals.ipynb
   ```

4. Follow the steps in the notebook to preprocess the data, train the model, and evaluate the results.

---

## Future Work

- **Expand the Dataset**: Include more examples of broken and sound plurals to improve model generalization.
- **Explore Other Architectures**: Experiment with Transformer-based models like BERT for this task.
- **Error Correction**: Develop post-processing techniques to fix common prediction errors.

---

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to enhance the project.

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes and push the branch:
   ```bash
   git commit -m "Add feature"
   git push origin feature-branch
   ```
4. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Special thanks to the creators of the **Hugging Face Transformers** library and **TensorFlow/Keras** for their powerful tools.
- Inspired by the rich morphology of the Arabic language and its computational challenges.

```

This README provides a comprehensive overview of the project, its structure, and how to get started. Let me know if you'd like to customize any section further!
```
