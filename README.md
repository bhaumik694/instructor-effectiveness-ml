# Instructor Effectiveness ML

A machine learning project that predicts **instructor effectiveness tiers** in an EdTech setting using learner outcomes, engagement metrics, and feedback data. Batch-level course data is aggregated to the instructor level and classified using Decision Tree and Random Forest models.

---

## Overview

Understanding instructor effectiveness is critical to improving learning outcomes at scale. This project builds a data-driven pipeline that aggregates batch-level course data up to the instructor level and trains classification models to predict whether an instructor falls into a High, Medium, or Low effectiveness tier.

The analysis is fully contained in a single Jupyter Notebook (`main.ipynb`) and operates on a structured dataset (`data.csv`) with ~2000 records.

---

## Repository Structure

```
instructor-effectiveness-ml/
├── data.csv          # Raw batch-level EdTech dataset
├── main.ipynb        # End-to-end analysis notebook
├── output.png        # Random Forest results / feature importance visualization
└── output_dt.png     # Decision Tree visualization
```

---

## Methodology

### 1. Data Aggregation
Batch-level records (individual course runs) are grouped and aggregated to the **instructor level**, computing summary statistics across metrics such as:
- Learner outcomes (completion rates, scores)
- Engagement metrics (session activity, interaction rates)
- Feedback/rating data

### 2. Target Engineering
Instructors are assigned an **effectiveness tier** (e.g., High / Medium / Low) based on their aggregated performance, forming the classification target.

### 3. Modeling
Two tree-based classification models are trained and evaluated:
- **Decision Tree Classifier** — interpretable baseline model, visualized in `output_dt.png`
- **Random Forest Classifier** — ensemble model for improved accuracy, with feature importance plotted in `output.png`

### 4. Evaluation
Models are assessed on standard classification metrics (accuracy, precision, recall, F1-score) using a train/test split.

---

## Getting Started

### Prerequisites

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### Run the Notebook

```bash
git clone https://github.com/bhaumik694/instructor-effectiveness-ml.git
cd instructor-effectiveness-ml
jupyter notebook main.ipynb
```

Run all cells in `main.ipynb` to reproduce the full analysis — from data loading and aggregation through model training and visualization.

---

## Results

| Model | Notes |
|---|---|
| Decision Tree | Interpretable; tree structure exported as `output_dt.png` |
| Random Forest | Higher accuracy ensemble; feature importances in `output.png` |

Visual outputs are saved as PNG files in the root directory.

---

## Tech Stack

- **Python** (Jupyter Notebook)
- **pandas** — data manipulation and aggregation
- **scikit-learn** — model training, evaluation
- **matplotlib / seaborn** — visualization

---

## Use Cases

- EdTech platforms evaluating instructor performance at scale
- HR/L&D teams building data-driven instructor feedback systems
- Researchers studying factors that drive learner outcomes

---

## License

This project is open source. See the repository for details.
