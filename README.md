# Laptop Price Predictor
This project aims to predict laptop prices based on various features like brand, screen size, resolution, RAM, CPU, storage, and other specifications. The dataset is cleaned, preprocessed, and fed into machine learning models to achieve accurate price predictions.

Table of Contents
- [Dataset](#Dataset)
- [Project Overview](#Project#Overview)
- [Installation](#Installation)
- [Usage](#Usage)
- [Modeling and Evaluation](#Modeling#and#Evaluation)
- [Results](#Results)
- [Contributing](#Contributing)
- [License](#License)

# Dataset

The dataset used in this project contains specifications and prices of laptops, including:

1. **Brand** (e.g., Dell, Apple)
2. **Type** (e.g., Gaming, Ultrabook)
3. **Screen Size & Resolution** (inches, PPI calculation)
4. **RAM** (in GB)
5. **CPU Brand** (e.g., Intel Core i5)
6. **Memory Type and Size** (e.g., HDD, SSD)
7. **Operating System (OS)**
8. **Weight** (kg)
9. **Price** (target variable)

Data was collected from an online marketplace and contains around 1300 entries.

# Project Overview
This project follows a series of steps to clean, analyze, and engineer features for the dataset before using it to train machine learning models:

# Data Cleaning: 
Removing unnecessary columns and cleaning data types.
# Feature Engineering: 
Creating new features, such as Pixels Per Inch (PPI) from screen resolution and Touchscreen/IPS flags.
# Exploratory Data Analysis (EDA): 
Visualizing distributions and relationships between features and price.
# Model Training: 
Implementing and evaluating multiple models to identify the best performance for predicting laptop prices.
# Installation
Clone this repository and install the dependencies:

```bash
git clone https://github.com/yourusername/laptop-price-predictor.git
cd laptop-price-predictor
pip install -r requirements.txt
```

# Usage
Run the Jupyter notebook to explore the data and train the model:

1. Open the notebook:
```bash
jupyter notebook Laptop_Price_Predictor.ipynb
```
2. Follow the cells to preprocess data, visualize patterns, and build machine learning models.
Alternatively, to predict a laptop price directly from the command line:

python
```bash
python predict.py --features "your feature values here"
```
#### Example Command:
```bash

python predict.py --brand "Dell" --ram 16 --cpu "Intel Core i5" --weight 1.5 --screen 15.6 --resolution "1920x1080" 
```
### Modeling and Evaluation
Various regression models were tested, including:

- [Linear Regression](#Linear#Regression)
- [Decision Tree Regressor](#Decision#Tree#Regressor)
- [Random Forest Regressor](#Random#Forest#Regressor)
- [XGBoost Regressor](#XGBoost#Regressor)

Performance was evaluated based on Mean Absolute Error (MAE) and R-squared scores. Hyperparameter tuning was done to improve accuracy.

## Results
The final model was able to achieve:

### - Mean Absolute Error (MAE): ~120 USD
### - R-squared: 0.85

This indicates that our model can reasonably predict prices within a narrow margin, making it useful for laptop price estimation based on given specifications.

# Contributing
If you wish to contribute, please fork the repository and submit a pull request with your proposed changes.

# License
This project is licensed under the MIT License.
