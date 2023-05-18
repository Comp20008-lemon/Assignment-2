# Canvas Group 80
# Group leader:  weishanl, weishan Liao
# Members: username, name
# Introduction of intended use for code and csv data files
The provided Python script is designed to analyze the nutritional data of protein-related food items. The accompanying .xlsx data file presents the data as follows:

- Each row represents a unique food item (including process, colors, and status).
- Each column represents different nutritional elements present in the food.

In the first part, we analyzed all nutrients by it's "score", the score is intended to suggests which data are more complete. So we marked all nutrients and gave them a relative score, where:
- 60% of the total score is based on the missing value ratio, where:
  - No missing value gives 6 scores.
  - Missing values less than 1% gives 5.85 scores.
  - Less than 2% gives 5.55 scores.
  - Less than 5% gives 5.15 scores.
  - Less than 10% gives 4.15 scores.
  - Less than 20% gives 2.15 scores.
- 40% of the total score is based on zero values, where:
  - No zero value gives 4 scores.
  - Less than 2% gives 3.92 scores.
  - Less than 5% gives 3.84 scores.
  - Less than 10% gives 3.60 scores.
  - Less than 20% gives 3.20 scores.
  - Less than 30% gives 2.40 scores.
  - Less than 40% gives 1.60 scores.
# Please note that this scoring is solely based on the data structure, so it might not always accurately reflect the data's quality.


# After this part, we picked only those nutrients with score higher than 9, and we got 20 nutrients.
# After the scoring part, we read researches and selected 6 out of the 20 nutrients
# # Setting the names of the nutirnts we intend to predict
The chosen nutrients for prediction are:
- 'Zinc (Zn) \n(mg)'
- 'Pyridoxine (B6) \n(mg)'
- 'Iron (Fe) \n(mg)'
- 'Potassium (K) \n(mg)'
- 'Magnesium (Mg) \n(mg)'
- 'Riboflavin (B2) \n(mg)'

After preprocessing the data, a correlation matrix is generated, and a linear regression model is trained on the data after scaling it using the MinMaxScaler. The model's performance is evaluated using metrics like R-squared and mean squared error (MSE), both on the test set and with 5-fold cross-validation.

# File structure and use of each file
1. The first file, `main.ipynb`, is the main file, containing all the code and comments. This file requires the pandas, numpy, seaborn, matplotlib, scikit-learn, scipy, and openpyxl libraries to run, as well as Jupyter Notebook.
2. The second file is the data file, an .xlsx file, containing all the nutrients we need to analyze.

# Instructions on how to run your code.
# open a jupyter notebook, and run the code in the main.ipynb file, it will generate the results and the findings we have.
# Any additional requirements needed to run code.
# We worked hard :b