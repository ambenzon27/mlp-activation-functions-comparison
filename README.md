# MLP Activation Function Benchmarking (repo is still in development)

This project benchmarks the effect of different activation functions—**Logistic**, **Tanh**, and **Leaky ReLU**—on the training performance of a Multilayer Perceptron (MLP) using backpropagation with momentum. Designed for educational and research purposes, it compares training efficiency and classification quality across activation types using precision metrics like **Accuracy**, **F1 Score**, and **Matthews Correlation Coefficient (MCC)**.

---

## Project Highlights

-  Two-layer MLP with user-configurable activations
-  Tracks Accuracy, F1 Score, and MCC over epochs
-  Implements gradient descent with momentum
-  Mini-batch training with learning curve visualization
-  Balanced synthetic or real multi-class dataset support
-  Activation-wise performance summary and plots

---

##  Repository Structure
- `README.md`
- `LICENSE`
- `requirements.txt`
- `data/`
  - `data.csv`
  - `data_labels.csv`
- `src/`
  - `train_mlp.py`
  - `model.py`
  - `backpropagation.py`
  - `metrics.py`
  - `data_loader.py`
  - `activation_functions.py`
  - `plotter.py`
  - `config.py`
- `experiments/`
  - `logistic/`
  - `tanh/`
  - `leaky_relu/`
- `figures/`
  - `learning_curves.png`
  - `summary_comparison.png`
  - `activation_table.md`
- `ANN.ipynb`
  


---

##  Example Results

| Activation   | Accuracy | F1 Score | MCC    |
|--------------|----------|----------|--------|
| Logistic     | 0.88     | 0.87     | 0.84   |
| Tanh         | 0.90     | 0.89     | 0.87   |
| Leaky ReLU   | 0.93     | 0.92     | 0.90   |

>  *Values are illustrative. See `/figures/` for real plots and results.*

---

##  Setup Instructions

### Install Dependencies
```bash
pip install ------

Prepare the Data
Put your data in the data/ folder:

data.csv: shape = [n_samples, n_features]

data_labels.csv: shape = [n_samples, 1]

Don't have data? Generate synthetic data:
python src/utils.py --generate-data


Train an MLP with a specific activation function:
python src/train_mlp.py --activation tanh


Supported activations:

- logistic
- tanh
- leakyrelu



