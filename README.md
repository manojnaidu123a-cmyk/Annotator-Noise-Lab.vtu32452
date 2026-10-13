# RLHF Against DPO Under Annotator Noise

**Student Name:** G MANOJ  
**Student ID:** VTU32452

## 1. Project Overview

This project studies the effect of annotator noise on preference learning by comparing two simplified approaches inspired by Reinforcement Learning from Human Feedback (RLHF) and Direct Preference Optimization (DPO).

The project simulates noisy human preference annotations at three noise levels: 0%, 10%, and 30%. It evaluates both approaches against synthetic gold preferences and displays the results using tables, graphs, and an interactive web application.

## 2. Objectives

- Study the impact of noisy preference annotations on model performance.
- Compare simplified RLHF-style and DPO-style approaches.
- Generate synthetic preference data and gold reward scores.
- Evaluate preference prediction accuracy.
- Measure ranking correlation between learned scores and gold rewards.
- Visualize experimental results at different noise levels.
- Understand the limitations of preference learning under noisy supervision.

## 3. Key Features

- Synthetic preference dataset generation.
- Configurable annotator noise levels.
- RLHF-style reward-model implementation.
- DPO-style pairwise preference-model implementation.
- Evaluation using held-out preference pairs.
- Preference accuracy and Spearman rank-correlation metrics.
- Performance comparison tables and graphs.
- Interactive Gradio dashboard.
- Reproducible experiments using a configurable random seed.

## 4. Technologies Used

- **Programming Language:** Python
- **Libraries:** NumPy, Pandas, SciPy, Scikit-learn, Matplotlib
- **Web Interface:** Gradio
- **Development Environment:** Google Colab / Jupyter Notebook
- **Version Control:** Git and GitHub

## 5. Project Methodology

1. Generate a synthetic dataset containing candidate answers and numerical features.
2. Assign gold reward scores to the candidates.
3. Generate preference pairs using the gold rewards.
4. Introduce annotator noise by randomly flipping a proportion of preference labels.
5. Train the simplified RLHF-style and DPO-style models.
6. Evaluate both approaches on held-out preference pairs.
7. Calculate preference accuracy and ranking correlation.
8. Compare model performance across different noise levels.
9. Present the results using tables, graphs, and the web interface.

## 6. Annotator Noise Levels

| Noise Level | Description |
|---|---|
| 0% | No intentional preference-label flipping |
| 10% | Approximately 10% of preference labels are flipped |
| 30% | Approximately 30% of preference labels are flipped |

These experiments help investigate how incorrect preference annotations influence learned reward scores and preference predictions.

## 7. Evaluation Metrics

### Preference Accuracy

Measures the proportion of held-out preference pairs for which the model correctly predicts the preferred candidate.

### Spearman Rank Correlation

Measures the agreement between the ranking produced by learned reward scores and the ranking produced by synthetic gold rewards.

### Performance Gap

The performance gap is calculated as:

`DPO-Style Accuracy - RLHF-Style Accuracy`

A positive value indicates higher accuracy for the DPO-style model, while a negative value indicates higher accuracy for the RLHF-style model.

## 8. How to Run the Project

### Option A: Google Colab

1. Open the project notebook from the GitHub repository.
2. Download the notebook or open it in Google Colab.
3. Run the cells in the correct order.
4. Install any required dependencies if prompted.
5. Execute the experiment and model-evaluation cells.
6. Run the Gradio application cell.
7. Open the generated application link, if available.
8. Review the results tables, comparison graphs, and experimental conclusions.

**Project Notebook:** [VTU32452_LLMPROJECT.ipynb](https://github.com/manojnaidu123a-cmyk/Annotator-Noise-Lab.vtu32452/blob/main/VTU32452_LLMPROJECT.ipynb)

### Option B: Run Locally

Clone the repository:

```bash
git clone https://github.com/manojnaidu123a-cmyk/Annotator-Noise-Lab.vtu32452.git
```

Navigate to the project directory:

```bash
cd Annotator-Noise-Lab.vtu32452
```

Install the dependencies:

```bash
pip install gradio numpy pandas matplotlib scikit-learn scipy jupyter
```

Launch the notebook:

```bash
jupyter notebook VTU32452_LLMPROJECT.ipynb
```

Run the notebook cells in order to execute the experiment.

## 9. Results and Discussion

The application compares the performance of the two simplified approaches at different annotator-noise levels.

The generated tables and graphs can be used to examine changes in preference accuracy, ranking correlation, and the performance gap as annotation noise increases.

**Note:** Actual numerical results and conclusions should be added only after successfully running the notebook and reviewing the outputs.

## 10. Limitations

- The dataset consists of synthetic preference annotations rather than real human feedback.
- The RLHF-style approach uses a simplified reward-model implementation.
- The DPO-style approach uses a simplified pairwise preference-model implementation.
- The project does not implement a complete language-model RLHF training pipeline or standard end-to-end DPO fine-tuning.
- Experimental results depend on the synthetic reward function, dataset, model configuration, and random seed.
- The findings should not be treated as a definitive real-world comparison of RLHF and DPO.

## 11. Conclusion

This project provides an experimental framework for understanding how annotator noise affects preference learning. By comparing simplified RLHF-style and DPO-style approaches across multiple noise levels, it helps analyze differences in preference prediction accuracy and ranking quality.

The final conclusions should be based on the results obtained by executing the experiments.

## 12. Repository Information

- **Project:** RLHF Against DPO Under Annotator Noise
- **Student:** G MANOJ
- **Student ID:** VTU32452
- **GitHub Repository:** [Annotator-Noise-Lab.vtu32452](https://github.com/manojnaidu123a-cmyk/Annotator-Noise-Lab.vtu32452)
- **Notebook:** [Open Jupyter Notebook](https://github.com/manojnaidu123a-cmyk/Annotator-Noise-Lab.vtu32452/blob/main/VTU32452_LLMPROJECT.ipynb)

---

*Academic Project — VTU32452*
