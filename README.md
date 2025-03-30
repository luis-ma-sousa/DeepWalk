# DeepGait – ML Classifier for Parkinson’s Motor Deficits

## 🐾 About the Data: MouseWalker Gait Tracking
The gait data used in this project was collected using MouseWalker, an open-source hardware and software system developed by César Mendes and colleagues at Columbia University (Mendes et al., 2015).

MouseWalker is a MATLAB-based tool that captures and analyzes high-resolution spatiotemporal gait parameters in freely walking rodents using a custom frustrated total internal reflection (fTIR) setup and high-speed video. The software tracks individual paw positions and body features frame-by-frame to extract over 70 locomotor metrics, including:

- Stance/swing cycles
- Inter-limb coordination
- Footprint clustering and gait phase
- Body and tail kinematics

📥 The raw data used in this project are output files from MouseWalker tracking, later processed for machine learning classification tasks.

## 🧠 Project Overview
This project was developed during my PhD to explore the potential of gait-based behavioral markers for neurodegenerative disease classification. Using extracted locomotor data, I trained and evaluated multiple classification models, achieving 91% accuracy with a neural network.

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
- **Normalizes** data using MinMax scaling  
- **Trains multiple ML classifiers** (MLP neural net, Random Forest, K-Nearest Neighbors, K-Means)  
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
