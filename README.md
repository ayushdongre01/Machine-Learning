# Machine Learning Notebooks

This repository is a **hands-on learning workspace** for core machine learning topics. Each topic lives in its own folder as **Jupyter notebooks** (`.ipynb`). Most notebooks build intuition with **NumPy** first, then show **scikit-learn** or **TensorFlow** where relevant.

---

## What's in this repo?

| Folder | Focus |
|--------|--------|
| [Regression](Regression/) | Linear regression from scratch, vectorization, multiple features, and scikit-learn |
| [Classification](Classification/) | Logistic regression: cost, gradients, regularization, and scikit-learn |
| [Neural Networks](Neural%20Networks/) | Calculus (SymPy), layers, activations, softmax, multiclass, and a coffee-roasting example |
| [Decision_Tree](Decision_Tree/) | Decision trees, random forests, and XGBoost |
| [Clustering](Clustering/) | K-means and anomaly detection (NumPy) |
| [Recommender_System](Recommender_System/) | Collaborative filtering, content-based (TF–IDF), and PCA |
| [Reinforcement_Learning](Reinforcement_Learning/) | Deep Q-Network (DQN) on Lunar Lander |

---

## How to run the notebooks

1. **Python 3.9+** is recommended (many stacks support 3.10–3.12; use versions your libraries support).

2. **Create a virtual environment** (optional but recommended):

   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. **Install the packages** needed for the notebooks you run. There is no single `requirements.txt` at the repo root; dependencies differ by notebook. A practical baseline:

   ```bash
   pip install jupyter numpy matplotlib scipy pandas scikit-learn sympy
   ```

   Add these **when you use the corresponding notebooks**:

   - **TensorFlow / Keras** (Neural Networks, some recommender notebooks): `pip install tensorflow`
   - **XGBoost** ([Decision_Tree/XGBoost.ipynb](Decision_Tree/XGBoost.ipynb)): `pip install xgboost`
   - **PyTorch + Gymnasium** ([Reinforcement_Learning/DQN_Lunar_Lander.ipynb](Reinforcement_Learning/DQN_Lunar_Lander.ipynb)): `pip install torch gymnasium`

4. **Start Jupyter** from the repo root so paths resolve consistently:

   ```bash
   jupyter notebook
   ```

   Or use **VS Code / Cursor** with the Jupyter extension and open any `.ipynb` file.

---

## Notebook index

### Regression

| Notebook | What it covers |
|----------|----------------|
| `Simple_Linear_Regression.ipynb` | One-variable linear regression with NumPy and plots |
| `Vectorization.ipynb` | Why vectorized NumPy is faster than Python loops |
| `Multiple_Linear_Regression.ipynb` | Multiple features, gradient descent style workflow |
| `Linear_regression_using_scikit_learn.ipynb` | `SGDRegressor`, scaling with `StandardScaler` |
| `houses.txt` | Sample data used with the regression notebooks |

### Classification

| Notebook | What it covers |
|----------|----------------|
| `Logistic_Regression.ipynb` | Logistic regression built from NumPy |
| `Logistic_cost_function.ipynb` | Cost function and visualization |
| `Regularized_Cost_and_Gradient.ipynb` | L2 regularization for logistic regression |
| `Logistic_Regression_using_scikit_learn.ipynb` | `LogisticRegression` from scikit-learn |

### Neural Networks

| Notebook | What it covers |
|----------|----------------|
| `Derivatives.ipynb` | Symbolic derivatives with SymPy |
| `Back_propagation.ipynb` | Chain rule and backprop ideas with SymPy + NumPy |
| `Neurons and Layers.ipynb` | Dense layers, sigmoid, losses in Keras |
| `Softmax.ipynb` | Softmax and a small Keras model |
| `Multiclass_classification.ipynb` | Multiclass setup with `make_blobs` and Keras |
| `Coffee_Roasting_using_Tensorflow.ipynb` | Binary classification with TensorFlow/Keras |
| `Coffee_Roasting_using_Numpy.ipynb` | Same-style problem with more manual NumPy/TensorFlow pieces |

### Decision Tree

| Notebook | What it covers |
|----------|----------------|
| `Decision_tree.ipynb` | `DecisionTreeClassifier` and accuracy |
| `Random_forest.ipynb` | `RandomForestClassifier`, one-hot encoding |
| `XGBoost.ipynb` | `XGBClassifier` and evaluation |

### Clustering

| Notebook | What it covers |
|----------|----------------|
| `K-means.ipynb` | K-means implemented or walked through with NumPy |
| `Anomaly_detection.ipynb` | Anomaly detection concepts with NumPy |

### Recommender System

| Notebook | What it covers |
|----------|----------------|
| `Collaborative_Filtering.ipynb` | Collaborative filtering (includes TensorFlow in later cells) |
| `Content_Based_Filtering.ipynb` | TF–IDF vectors and cosine similarity |
| `PCA.ipynb` | Standardization and PCA with scikit-learn |

### Reinforcement Learning

| Notebook | What it covers |
|----------|----------------|
| `DQN_Lunar_Lander.ipynb` | DQN with PyTorch on **Gymnasium** `LunarLander-v3`: replay buffer, target network (soft updates), epsilon decay |

**Note:** Lunar Lander training can take noticeable time on CPU; a CUDA GPU speeds up PyTorch if available.

---

## Folder and file notes

- **`Neural Networks`** has a space in the name. On the command line, quote the path or use tab completion.
- **`.ipynb_checkpoints`** folders are created by Jupyter when you edit notebooks. They are local editor artifacts; you can add them to `.gitignore` if you do not want them in version control.
- Notebooks are **educational**: they mix theory, small datasets, and standard library APIs. They are not a single deployable application.

---

## Suggested study order

If you want a linear path through the material:

1. Regression → Classification  
2. Neural Networks (Derivatives → Back_propagation → Neurons and Layers → Softmax → Multiclass)  
3. Decision_Tree → Clustering  
4. Recommender_System  
5. Reinforcement_Learning (after you are comfortable with neural nets and training loops)

Adjust the order to match your course or project needs.
