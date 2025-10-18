# DeepGait – ML Classifier for Parkinson’s Motor Deficits



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

## 🔧 Tools & Technologies
- Python (Jupyter Notebooks)
- pandas, NumPy, scikit-learn, TensorFlow
- Matplotlib, Seaborn (for visualizations)

## 📁 Project Structure
```
DeepGait/
├── data/               
├── notebooks/          
└── README.md          
```


## 📊 What the Notebook Does
- **Imports and explores** gait data from preprocessed MouseWalker CSV files  
- **Performs data cleaning** and feature selection (including variance and correlation filtering)   
- **Trains multiple ML classifiers** (Neural net, Random Forest)  
- **Compares model performance** across accuracy, F1 score, and confusion matrices  
- **Visualizes results** using Seaborn and Matplotlib (heatmaps, barplots, accuracy metrics)

## 🚀 How to Run

1. Clone this repo or download the notebook
2. Place the processed CSV data in the `/data` directory
3. Open `notebooks/DeepWalk_v01.ipynb` in Jupyter or Colab
4. Run all cells to reproduce preprocessing, training, and evaluation

## 📌 Status

Finalized for demo and portfolio use. Future updates may include a live dashboard and additional behavioral classifiers.

## 🧑‍💻 Author
Luís Sousa — [LinkedIn](https://www.linkedin.com/in/luis-ma-sousa31) | [GitHub](https://github.com/luismasousa)
