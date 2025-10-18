# DeepWalk – ML Classifier for Parkinson’s Motor Deficits



https://github.com/user-attachments/assets/282e9eb1-e725-449f-a9cc-db1ecba97a5c



## 🐾 About the Data: MouseWalker Gait Tracking
The gait data used in this project was collected using **MouseWalker**, an open-source hardware and software system developed by [Prof. César Mendes](https://github.com/NeurogeneLocomotion) and colleagues at Columbia University ([Mendes et al., 2015](https://doi.org/10.1186/s12915-015-0154-0)).

MouseWalker is a MATLAB-based tool that captures and analyzes high-resolution spatiotemporal gait parameters in freely walking rodents using a custom frustrated total internal reflection (fTIR) setup and high-speed video. The software tracks individual paw positions and body features frame-by-frame to extract 86  locomotor metrics, including:
- Stance/swing cycles
- Inter-limb coordination
- Footprint clustering and gait phase
- Body and tail kinematics

<img width="395" alt="Screenshot 2025-03-30 at 17 41 20" src="https://github.com/user-attachments/assets/08a3507d-51bd-4897-a2fa-6588419e6ac0" />

From (Mendes et al., 2015).



📥 The raw data used in this project are output files from MouseWalker tracking, later processed for machine learning classification tasks.

## 🧠 Project Overview
This project was developed during my PhD under the supervision of [Prof. Hugo Vicente Miranda](https://www.linkedin.com/in/hugo-vicente-miranda-3b5b661/) to explore the potential of gait-based behavioral markers for neurodegenerative disease classification. Using extracted locomotor data, I trained and evaluated multiple classification models, achieving 95% accuracy with a neural network.

The project implements a modular, end-to-end workflow composed of three main stages:

1. **Data Pre-processing**  
   - Ingests raw MouseWalker outputs.  
   - Identifies and removes statistical outliers with robust methods (FDR-controlled).  
   - Performs median imputation and covariate correction (speed, body weight, body length).  
   - Normalises locomotor features to generate a clean, standardised dataset for further analysis.  

2. **Statistical Analysis**  
   - Mixed-effects modelling (`Y ~ Age × Genotype × Diet + (1|AnimalID)`) to detect main effects and interactions.  
   - ANOVA fallback for variables not suitable for mixed modelling.  
   - Log₂ fold-change visualisations, PCA analysis, and feature-level interpretation.  

3. **Machine Learning Classification**  
   - Dimensionality reduction via PCA and variance filtering.  
   - Multi-class classification using **Residual Neural Networks** and **Random Forests**.  
   - Automated hyperparameter tuning, early stopping, and learning-rate scheduling.  
   - Model interpretability through **permutation-based feature importance**.  
   - Confusion matrices and cross-validation metrics (accuracy, F1-score) for model evaluation.  
---

## 🧩 Key Findings (in simple terms)

1. **Gait can reveal brain changes before symptoms appear.**  
   Subtle differences in how mice walk can signal early neural or metabolic alterations long before visible motor deficits emerge.

2. **Machine learning uncovered a new molecular player in motor control.**  
   By analysing locomotor patterns with advanced models, this work identified a previously unrecognised protein as a key regulator of movement and a potential contributor to Parkinson’s disease mechanisms.

3. **The models reached high classification accuracy.**  
   Using behavioural data alone, the best neural network achieved approximately **95% accuracy** in distinguishing experimental conditions, demonstrating that gait-based features are highly predictive of underlying biological states.

4. **The workflow bridges neuroscience and AI.**  
   DeepWalk shows how computational tools can transform complex behavioural datasets into biologically meaningful insights, providing a reproducible framework for studying neurodegenerative disorders.

---
## 🔒 Data and notebooks Availability

Due to the unpublished nature of this research, raw and processed data, as well as the original notebooks, are not included in this repository.  

➡️ **Access can be provided upon reasonable request.**

---

## 🧰 Tools & Technologies

- **Languages:** Python 3.9  
- **Libraries:** pandas, NumPy, scikit-learn, TensorFlow/Keras  
- **Visualisation:** Matplotlib, Seaborn  
- **Statistics:** statsmodels
- **Environment:** Jupyter Notebooks  

---

## 📁 Repository Structure
```
DeepWalk/
├── data/                   # Processed MouseWalker data
├── notebooks/              # Jupyter notebooks (preprocessing, stats, ML)
│   ├── DeepWalker - Data Pre-processing pipeline.ipynb
│   ├── DeepWalker - Statistical analysis pipeline.ipynb
│   └── DeepWalker - Machine Learning analysis pipeline.ipynb
└── README.md
```
## 📌 Status

Finalized for demo and portfolio use. Future updates may include a live dashboard and additional behavioral classifiers.

> 🧩 **Future release:**  
> Once the study is published, all source code, notebooks, and raw data will be made publicly available here.


## 🧑‍💻 Author
Luís Sousa — [LinkedIn](https://www.linkedin.com/in/luis-ma-sousa31) | [GitHub](https://github.com/luismasousa)
