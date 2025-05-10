# SMILES-Based Molecular Property Prediction and Molecule Generation

This project investigates how different SMILES embeddings influence molecular property prediction using XGBoost and explores various techniques to generate novel molecules. The study compares the effectiveness of One-hot, Morgan Fingerprints, ChemBERTa, BERT, and TransPolymer embeddings, and evaluates molecule generation using N-gram, RNN, and Transformer-based models.

---

## Objectives

- **Embed SMILES strings** using:
  - One-hot encoding
  - Morgan Fingerprints
  - ChemBERTa
  - BERT
  - TransPolymer

- **Train XGBoost models** to predict molecular properties based on each embedding.

- **Generate new molecules** using:
  - N-gram models (with varying N values)
  - Recurrent Neural Networks (RNN)
  - Transformer-based models

- **Evaluate generated molecules** on:
  - **Validity** – Are the generated SMILES syntactically and chemically valid?
  - **Novelty** – Are the molecules new? (Tanimoto similarity with training set)
  - **Uniqueness** – Are the generated molecules distinct from each other?

---

## Evaluation Metrics

### Prediction Task (XGBoost)

- R² Score
- Mean Absolute Error (MAE)

### Generation Task

- **Validity**: Percentage of valid SMILES strings.
- **Novelty**: Fraction of generated molecules that are not similar to training data (Tanimoto-based).
- **Uniqueness**: Fraction of non-duplicate molecules in the generated set.

---

## Experimental Variations

- N-gram models are trained with `N` ranging from 2 to 20.
- The impact of `N` on validity, novelty, and uniqueness is analyzed and visualized.
- Performance of embeddings is compared by evaluating predictive accuracy on a downstream task using XGBoost.

---

## Technologies Used

- **RDKit** – For SMILES parsing, molecule validity, and similarity computation.
- **XGBoost** – For regression modeling.
- **Transformers / Hugging Face** – For ChemBERTa and BERT-based embeddings.
- **PyTorch / TensorFlow** – For RNN and Transformer models.
- **Matplotlib / Seaborn** – For visualizations.

---



