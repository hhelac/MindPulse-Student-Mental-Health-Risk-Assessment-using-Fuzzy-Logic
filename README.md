# MindPulse: Student Mental Health Risk Assessment using Fuzzy Logic 🧠📊

An advanced **Fuzzy Inference System (FIS)** designed to evaluate and predict the level of mental health intervention needed for university students. 

Built using a real-world **Kaggle Dataset (2025 Student Mental Health Survey)**, this project models complex, subjective, and non-binary human emotions (like anxiety, isolation, and academic pressure) into a structured mathematical framework using Mamdani-style fuzzy inference.

## 🚀 Project Overview

Evaluating mental health risk is inherently challenging due to the ambiguity and subjectivity of human feelings. This project leverages **Fuzzy Logic** to transcend traditional binary thresholds, mapping continuous real-world data into linguistic variables to approximate human-like diagnostic reasoning.

### Key Implementation Steps:
- **Data Engineering & Cleaning:** Processed survey metrics, handled missing data (`fillna`), transformed categorical ranges into discrete numeric attributes, and inverted metrics (e.g., social relationship scales) for logical engineering consistency.
- **Fuzzification & Domain Modeling:** Defined input/output membership functions (utilizing triangular shapes `trimf`) across 8 core student lifeworld dimensions (Anxiety, Depression, Sleep Patterns, Academic Pressure, Social Relationships, Isolation, Financial Concerns, and Future Insecurity).
- **Complex Knowledge Base (Fuzzy Rules):** Formulated an extensive rule matrix combining multi-variable logic using intersection (`&`), union (`|`), and negation (`~`) operators to split target risk into *Minimal*, *Moderate*, and *High* intervention categories.
- **Defuzzification & Interactive Simulation:** Integrated a dynamic command-line runtime simulation (`ControlSystemSimulation`) that computes exact risk percentages and visualizes output trends dynamically.

## 🛠️ Tech Stack & Libraries

- **Language:** Python 3
- **Environment:** Google Colab / Jupyter Notebook
- **Core AI Library:** `scikit-fuzzy` (`skfuzzy`)
- **Data Science Toolkit:** `pandas`, `numpy`, `matplotlib`

## 📊 Live System Demo & Evaluation

The notebook contains an interactive testing framework (`run_custom_fuzzy_system()`) that prompts for live student profile parameters and computes real-time predictions:

```python
# System Sample Execution
Unesite vrijednosti (0-10 ili 3-8 za spavanje):
Anksioznost (0-10): 7.5
Depresija (0-10): 6.0
Prosječan broj sati sna (3-8): 4.5
...
Procijenjena potreba za intervencijom: 78.42/100
