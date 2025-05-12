# Recidivism_project

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

Predicting recidivism using machine learning

---

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│       └── Unfilterdata.csv
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
├── models             <- Trained and serialized models, model predictions, or model summaries
├── notebooks          <- Jupyter notebooks (e.g., `1.0-initial-data-exploration.ipynb`)
├── pyproject.toml     <- Project configuration
├── references         <- Data dictionaries, manuals, and other explanatory materials.
├── reports            <- Generated analysis as HTML, PDF, etc.
│   └── figures        <- Generated graphics and figures
├── requirements.txt   <- The requirements file for environment setup
├── setup.cfg          <- Configuration for flake8, etc.
├── tests              <- Unit tests for line testing the code
│   └── test_rehab_model.py
└── recidivism_predictor   <- Source code for this project
    ├── __init__.py
    ├── config.py
    ├── dataset.py
    ├── features.py
    ├── modeling
    │   ├── __init__.py 
    │   ├── predict.py
    │   └── train.py
    └── plots.py
```

---

## 📊 Overview

This project builds and compares machine learning models to predict recidivism — the tendency of a convicted criminal to reoffend. The goal is to support better targeting of rehabilitation services and reduce repeated incarceration.

---

## 📦 Setup

1. **Clone the repo and create a virtual environment**
```bash
git clone https://github.com/msomakpo/recidivism-risk-prediction/tree/main
cd recidivism-risk-prediction
python -m venv venv
source venv/bin/activate  # or `venv\Scripts\activate` on Windows
pip install -r requirements.txt
```

2. **Run the main notebook**
```bash
jupyter notebook notebooks/recidivism_analysis.ipynb
---

## 🧪 Line Testing with Pytest

Basic line tests for feature engineering, data cleaning, and model training:
```bash
pip install pytest
pytest tests/
```

---

## 📚 Citations

- National Institute of Justice. (2024, September 5). *NIJ’s Role Under the First Step Act*. https://nij.ojp.gov/topics/corrections/nijs-role-under-first-step-act  
- Qlik. (2025, March 16). *What is Predictive Modeling? Types & Techniques*. https://www.qlik.com/us/predictive-analytics/predictive-modeling  
- Wikipedia Contributors. (n.d.). *COMPAS (software)*. Wikimedia Foundation. https://en.wikipedia.org/w/index.php?title=COMPAS_(software)&oldid=1280320823  
- Berk, R., Heidari, H., Jabbari, S., Kearns, M., & Roth, A. (2020). *Fairness in Criminal Justice Risk Assessments: The State of the Art*. https://hdsr.mitpress.mit.edu/pub/hzwo7ax4/release/7  
- Mitchell, M. (2014, October 31). *4 Ways States Can Reduce Incarceration Rates*. https://www.cbpp.org/blog/4-ways-states-can-reduce-incarceration-rates  
- Pettit, B., & Gutierrez, C. (2018). *Mass Incarceration and Racial Inequality*. *American Journal of Economics and Sociology*, 77(3–4), 1153–1182. https://doi.org/10.1111/ajes.12241  
- Merriam-Webster. (2019). *Definition of Recidivism*. https://www.merriam-webster.com/dictionary/recidivism  
- Miller, G. (2022, March 18). *The Invention of Incarceration*. JSTOR Daily. https://daily.jstor.org/the-invention-of-incarceration/

---

## ⚖️ Ethical Considerations

Predictive models in criminal justice risk reinforcing systemic biases. We use interpretable models, fairness-aware metrics, error analysis on misclassified cases, and include ethical oversight recommendations in this project. These tools must be implemented responsibly.
