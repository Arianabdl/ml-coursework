# ID3 Decision Tree from Scratch

Two parts, on two UCI datasets (**Car Evaluation** and **Nursery**, downloaded directly from the UCI repository in the notebook).

**Part 1 — ID3 from scratch**
- Entropy and information gain implemented by hand to choose splits
- **Reduced Error Pruning** on a validation set to limit overfitting
- Pruned vs. unpruned tree compared

**Part 2 — scikit-learn baseline**
- `DecisionTreeClassifier(criterion="entropy")` with label encoding
- Hyperparameter tuning with cross-validation, evaluation with a confusion matrix

Notebook: [`id3_from_scratch.ipynb`](id3_from_scratch.ipynb)
