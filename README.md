# Social Media Impact Analysis for Food Pantries
## Dependencies
[![Pandas](https://img.shields.io/badge/pandas-1.3.3-blue)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-1.21.4-blue)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/matplotlib-3.4.3-blue)](https://matplotlib.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-blue)](https://scikit-learn.org/)
[![SciPy](https://img.shields.io/badge/scipy-1.7.3-blue)](https://www.scipy.org/)
## Overview
This repository contains the code and analysis for a research project aimed at enhancing social media impact for food safety security organizations. The project focuses on understanding text tone preferences based on user demographics using machine learning techniques.

## Project Structure

### File Combiner.ipynb
The file_combiner.ipynb notebook serves the purpose of combining two datasets generated from testing a survey web application. The objective is to create a final Excel dataset comprising 50 data points. This initiative is driven by the intention to test machine learning clustering models with larger datasets. Although the ultimate goal is to train the models with real survey responses in the future, the immediate focus is on experimenting with larger numbers than the initial dataset's 15 data points.

Key Steps in the Notebook:

1. Loading the Datasets:<br>
The notebook likely starts by loading the two datasets generated from testing the survey web application. These datasets could be in the form of Excel files, CSV files, or any other format suitable for data storage.<br>

2. Data Combination:<br>
The datasets are combined, and the notebook uses pandas or a similar data manipulation library to concatenate or merge the dataframes. The specific method depends on the structure of the datasets and the desired way of combining them.<br>

3. Dataset Size Expansion:<br>
The primary goal is to increase the size of the dataset from the original 15 data points to 50 data points. This might involve duplicating or augmenting the existing data in a controlled manner to maintain data integrity and relevance.<br>

4. Exporting the Final Dataset:<br>
Once the datasets are combined and expanded, the notebook exports the final dataset to a new Excel file. This file serves as the larger dataset with 50 data points and can be used for testing machine learning clustering models.

### Data-analysis.ipynb

1. Data Collection
- Raw data obtained from a survey consisting of demographic information and user preferences for text tonality.

2. Data Preprocessing
- Cleaning, encoding, and feature engineering tasks to prepare the dataset for analysis.

3. Exploratory Data Analysis (EDA)
- In-depth exploration of the dataset, including descriptive statistics, distribution of tonality preferences, and identification of patterns.

4. Clustering Analysis
- Application of hierarchical clustering algorithm to identify significant patterns among different demographic groups.

5. Model Training and Evaluation
- Building machine learning models to predict tonality preferences based on demographic features.

6. Results and Insights
- Summary of findings, including distinct tonality preferences within demographic clusters.

## Kmeans without PCA
![image](https://github.com/esoto15/text-tone-preference-analysis/assets/106943089/39824d46-8f7d-4d1a-a2cf-26e055470f17)
## Kmeans with PCA
![image](https://github.com/esoto15/text-tone-preference-analysis/assets/106943089/cad67eed-e23a-435f-b58d-ce0f65e0cf79)

## Requirements
- Python 3.x
- Required libraries are listed in `requirements.txt`. Install them using `pip install -r requirements.txt`.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo.git
