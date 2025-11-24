# Fatigue Life Prediction Analysis  
# fatigue-life-prediction

**Project for Capstone Assignment 20.1: Initial Report and Exploratory Data Analysis (EDA)**  
_First Capstone Modeling & EDA Assignment_  
Course: **Professional Certificate in Machine Learning and Artificial Intelligence by Berkeley**  
**By: Erfan Maleki**

---

##  Overview
This project investigates the **fatigue behavior of LPBF-manufactured AlSi10Mg alloy** using a comprehensive experimental dataset that includes process parameters, surface characteristics, and mechanical testing variables.  

The assignment focuses on performing **Exploratory Data Analysis (EDA)**, cleaning the dataset, engineering useful features, and developing a **baseline regression model** for fatigue life prediction.

Dataset used:  
**Capstone data – Fatigue of LPBF AlSi10Mg.xlsx**
data adopted from: https://www.sciencedirect.com/science/article/pii/S2214860424002252

---

##  Objective
The main objectives of this project are:

- Perform complete **EDA** to understand patterns in surface roughness, process parameters, and fatigue behavior.  
- Clean and preprocess the dataset (missing values, duplicates, outliers).  
- Engineer features such as **energy density**, **log-transformed fatigue life**, and **roughness groups**.  
- Develop a **baseline regression model** for predicting fatigue life.  
- Identify the **most influential variables** affecting fatigue performance.

---

##  Dataset Details
The dataset includes the following feature groups:

### **Manufacturing & Treatment Variables**
- Build orientation  
- Surface condition (as-built, machined, shot-peened, etc.)  
- Heat treatment data  

### **Process Parameters**
- Laser power  
- Scan speed  
- Layer thickness  
- Hatch distance  
- Relative density  
- Volumetric energy density (VED) — engineered feature  

### **Surface & Microstructure Features**
- Sa, Sv, Sp, Sz roughness parameters  
- Porosity measurements  
- Defect metrics (if available)

### **Mechanical Testing Inputs**
- Stress amplitude  
- R-ratio  
- Testing frequency  

### **Target Variable**
- **Fatigue Life (Nf)** — number of cycles to failure (regression target)

---

##  Tools and Libraries
- **Python**
- **pandas** – Data cleaning and preprocessing  
- **numpy** – Numerical operations  
- **matplotlib & seaborn** – EDA visualizations  
- **scikit-learn** – Baseline regression model  
- **Jupyter Notebook** – Full analysis workflow

---

##  Key Insights
- Surface condition is one of the strongest predictors of fatigue life.  
- Higher surface roughness (especially **Sa** and **Sz**) is associated with lower fatigue resistance.  
- Stress amplitude shows a clear inverse relationship with fatigue life.  
- Volumetric energy density and porosity provide insight into part quality and performance.  
- Outlier analysis reveals several extreme fatigue cases likely tied to defects or unusual test conditions.

---

##  Baseline Model Summary

A baseline **Linear Regression** model was developed using cleaned and engineered features.

### **Evaluation Metric**
- **R² Score** — selected to quantify how well the model explains variability in fatigue life.

### **Result Summary**
- The baseline model produces a **moderate R²**, confirming that linear relationships exist but are insufficient alone.  
- Nonlinear models (Random Forest, Gradient Boosting, XGBoost) will be explored in Module 24 to improve predictive accuracy.  

---

##  Repository Structure

| File                                           | Description                                                   |
|-----------------------------------------------|--------------------------------------------------------------|
| `Capstone_20_1_EDA.ipynb`                     | Main Jupyter Notebook with EDA and baseline regression model |
| `Capstone data- Fatigue of LPBF AlSi10Mg.xlsx` | Dataset used in the project                                  |
| `Fatigue_Capstone_Initial_Report.docx`        | Full report with figures and discussion                      |
| `README.md`                                   | Project description and instructions                         |
| `LICENSE`                                     | MIT License (optional)                                       |

---

## How to Run
1. Clone the repository:

```bash
git clone https://github.com/erfmlk/fatigue-life-prediction.git
cd fatigue-life-prediction
