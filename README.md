# Enhancing Social Media Impact: Leveraging User Demographics for Text Tone Preference Analysis

## Abstract
This study investigates the correlation between user demographics and text tone preferences for social media content aimed at addressing food insecurity among Hispanic households in the United States. Using k-means and hierarchical clustering machine learning models, we analyze preliminary data collected from a research group comprising mentors and students who tested the survey framework. By developing various text tone connotations, we aim to uncover patterns in post preferences among the Hispanic community. Our findings will assist food pantries in crafting more engaging and effective social media content.

## Dependencies
![](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![](https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![](https://img.shields.io/badge/NumPy-013243.svg?style=for-the-badge&logo=NumPy&logoColor=white)
![](https://img.shields.io/badge/scikitlearn-F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![](https://img.shields.io/badge/SciPy-8CAAE6.svg?style=for-the-badge&logo=SciPy&logoColor=white)
![](https://img.shields.io/badge/Plotly-3F4F75.svg?style=for-the-badge&logo=Plotly&logoColor=white)
![](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![](https://img.shields.io/badge/Microsoft%20Excel-217346.svg?style=for-the-badge&logo=Microsoft-Excel&logoColor=white)
## Keywords
Food Insecurity, Text tone preferences, K-Means, Hierarchical Clustering, Unsupervised Learning

## Data Preprocessing Pipeline

| age    | gender | ethnicity     | race           | education    | marital_status | income             | employment         | language | disability          | states  | sample_1 | sample_2 | sample_3 | sample_4 | sample_5 | sample_6 | sample_7 | sample_8 |
|--------|--------|---------------|----------------|--------------|----------------|--------------------|--------------------|----------|---------------------|---------|----------|----------|----------|----------|----------|----------|----------|----------|
| 45-54  | female | non hispanic  | native american| High School  | na             | $25,000 - $49,999  | Employed Part time| both     | i do not have a disability | indiana | Persuasive | Simpler  | Empathetic | Persuasive | Original | Original | Persuasive | Original |
| 18-24  | male   | hispanic      | white          | High School  | single         | Less than $25,000  | Employed Part time| english  | i do not have a disability | illinois | Original | Simpler  | Empathetic | Simpler    | Simpler   | Original | Original   | Persuasive |
| 25-34  | female | non hispanic  | multiracial    | Associate    | single         | Less than $25,000  | Student            | english  | i do not have a disability | new York | Original | Original | Simpler    | Simpler    | Empathetic | Empathetic | Empathetic | Simpler   |

**Figure 1.1** Initial dataset
### Combining Post Preferences and Attribute Selection

To simplify data analysis and model training, the **melt** function was utilized to combine individual post choices from multiple columns ('sample_1' to 'sample_8') into a single 'choice' column. This effectively reduced the dataset's dimensionality while preserving crucial demographic information such as age, gender, ethnicity, education, income, employment status, and disability.Each row in the dataset represents an individual submission, with the 'choice' column indicating the preferred post option. This implementation facilitates the examination of individual user preferences while considering demographic characteristics.  

| age    | gender | ethnicity     | education   | income             | employment         | disability          | choice     |
|--------|--------|---------------|-------------|--------------------|--------------------|---------------------|------------|
| 45-54  | female | non hispanic  | High School | $25,000 - $49,999  | Employed Part time| i do not have a disability | Persuasive |
| 18-24  | male   | hispanic      | High School | Less than $25,000  | Employed Part time| i do not have a disability | Original   |
| 25-34  | female | non hispanic  | Associate   | Less than $25,000  | Student            | i do not have a disability | Original   |

### Encoding Categories
| **Age Category**       | **Encoded Value (Age)** | **Income Category**   | **Encoded Value (Income)** | **Disability Category**          | **Encoded Value (Disability)** | **Ethnicity Category**       | **Encoded Value (Ethnicity)** |
|------------------------|--------------------------|------------------------|-----------------------------|--------------------------------|--------------------------------|--------------------------------|----------------------------|
| 18-24                  | 0                        | Less than 25000        | 0                           | No                             | 0                              |Hispanic                     | 1                            |
| 25-34                  | 1                        | 25000 - 49999          | 1                           | Yes                            | 1                              |Non-Hispanic                 | 0                              |
| 35-44                  | 2                        | 50000 - 74999          | 2                           | Prefer not to say              | -1                             |Prefer not to say            | -1                              |
| 45-54                  | 3                        | 75000 - 99999          | 3                           |         -                       |           -                     |           -                     |           -                     |
| 55-64                  | 4                        | 100000 - 149999        | 4                           |         -                       |           -                     |           -                     |           -                     |
| 65 and above           | 5                        | 150000 or more         | 5                           |          -                      |           -                     |           -                     |           -                     |
| Prefer not to say      | -1                       | Prefer not to say      | -1                          |          -                      |           -                     |           -                     |           -                     |





