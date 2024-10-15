# Netflix Movie Recommendations
This project implements a movie recommendation system using the Apriori algorithm. The system identifies movie-watching patterns and generates recommendations based on association rules.

## Features
Apriori Algorithm: Used to mine frequent itemsets and generate association rules between movies.
Movie Dataset: The dataset contains user transactions of movies watched, extracted from a provided Excel file.
Recommendations: Generates recommendations based on minimum support, confidence, and lift.
## Installation
To run this project, you need to install the following dependencies:
1. Clone the repository or download the project files.
2. Install the required Python libraries
   pip install pandas numpy matplotlib apyori

### Usage
Load the dataset:

The project uses an Excel dataset named Netflix_Recommandation.xlsx. You need to ensure this file is present in the project directory or provide the correct path in the notebook.

### Run the Jupyter notebook:
Open the Netflix_Movie_Recommendations.ipynb file in Jupyter Notebook or Google Colab.

Execute the cells to:
Load and preprocess the data
Apply the Apriori algorithm
Generate movie recommendations based on the rules

## Apriori Algorithm Parameters
Support: Minimum support of 0.003
Confidence: Minimum confidence of 0.2
Lift: Minimum lift of 3
Max Length: Maximum length of 2 items in a rule
You can modify these parameters to tweak the recommendation results.

## Results
The Apriori algorithm outputs association rules that reveal patterns in movie-watching behavior. For example, if a user watches movie X, they are likely to watch movie Y, based on the extracted rules.
