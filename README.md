# RLHF Against DPO Under Annotator Noise

**Student Name:** G MANOJ  
**Student ID:** VTU32452

## 📌 Project Overview

This project investigates how annotator noise affects preference learning by comparing two simplified approaches inspired by Reinforcement Learning from Human Feedback (RLHF) and Direct Preference Optimization (DPO).

The application simulates noisy human preference annotations at three different noise levels: **0%, 10%, and 30%**. It evaluates both approaches against clean synthetic gold preferences and displays the results through an interactive web dashboard.

## 🎯 Objectives

- Simulate human preference annotations with different levels of noise.
- Compare RLHF-style and DPO-style preference-learning models.
- Evaluate model accuracy against clean gold preferences.
- Measure ranking correlation between predicted scores and gold rewards.
- Visualize the performance gap using graphs and result tables.
- Generate an experimental conclusion based on the observed results.

## ✨ Features

- Interactive web application built with Gradio.
- Configurable annotator noise levels.
- Synthetic preference dataset generation.
- RLHF-style linear reward-model proxy.
- DPO-style nonlinear direct preference-model proxy.
- Held-out preference accuracy evaluation.
- Spearman ranking-correlation analysis.
- Automatic performance comparison graph.
- Generated experimental conclusion.
- Adjustable random seed for reproducible experiments.

## 🛠️ Technologies Used

- **Python** — Core programming language
- **NumPy** — Numerical computations and synthetic data generation
- **Pandas** — Experimental result management
- **Scikit-learn** — Machine-learning models
- **SciPy** — Ranking-correlation calculations
- **Matplotlib** — Data visualization
- **Gradio** — Interactive web interface
- **Google Colab** — Cloud-based execution environment

## 🔬 Experimental Methodology

The project follows these steps:

1. Generate 200 synthetic candidate answers with six numerical features each.
2. Assign a synthetic gold reward to every candidate.
3. Generate preference pairs using the gold rewards.
4. Introduce annotator noise by randomly reversing some preference labels.
5. Train the two simplified preference-learning models.
6. Evaluate their predictions on clean held-out preference pairs.
7. Compare accuracy, ranking correlation, and the performance gap.
8. Display the experimental results in the web application.

## 📊 Noise Levels

| Noise Level | Description |
|---|---|
| 0% | No intentional preference-label flipping |
| 10% | Approximately 10% of preferences are flipped on average |
| 30% | Approximately 30% of preferences are flipped on average |

## 📈 Evaluation Metrics

**1. Held-out Preference Accuracy**

Measures the fraction of test pairs for which the model predicts the correct winner according to the gold reward.

**2. Ranking Correlation**

Uses Spearman correlation to measure how closely the learned reward scores rank candidates compared with their gold rewards.

**3. Performance Gap**

Calculated as:

`Performance Gap = DPO-Style Accuracy - RLHF-Style Accuracy`

A positive gap indicates that the DPO-style proxy has higher accuracy in that experiment. A negative gap indicates that the RLHF-style proxy has higher accuracy.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook.
3. Copy the complete project code into a code cell.
4. Run the cell and wait for the required packages to install.
5. Open the Gradio share link displayed in the output.
6. Select the noise levels and click **Run Experiment**.
7. View the results table, graph, and generated conclusion.

### Option 2: Run Locally

**Step 1: Clone the repository**

```bash
git clone https://github.com/kusumakureti47/rlhf-vs-dpo-annotator-noise.git
```

**Step 2: Open the project directory**

```bash
cd rlhf-vs-dpo-annotator-noise
```

**Step 3: Install dependencies**

```bash
pip install gradio numpy pandas matplotlib scikit-learn scipy
```

**Step 4: Run the application**

Save the application code in a Python file named `app.py`, then execute:

```bash
python app.py
```

Open the local URL displayed in the terminal.

## 📋 Results

The application produces a comparison table and a bar chart for the selected noise levels.

The experiment helps investigate whether increasing annotator noise changes the relative performance of the two approaches. Actual results should be recorded after running the application.

## ⚠️ Limitations

This project is an educational synthetic simulation.

- The dataset is generated artificially.
- The RLHF-style implementation uses a simplified linear reward model.
- The DPO-style implementation uses a simplified nonlinear pairwise preference model.
- Neither implementation represents a complete RLHF or standard DPO training pipeline for a language model.
- Results depend on the synthetic reward function, feature representations, training settings, and random seed.

Therefore, the findings should not be interpreted as a definitive real-world comparison of
