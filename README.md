# Charity Funding Predictor

Prepared by Corey Lawson-Enos

## Overview
* A TensorFlow, neural network, binary classification model used to predict if a funded organization will be successful based on the features in the test charity's dataset.

## Technologies
Pandas, TensorFlow, Scikit-learn, Jupyter Notebook

## Access/Resources
* Data source: 'charity_data.csv' file saved to Resources folder in this repository. 
* Initial Test Study Files:
    - Use 'AlphabetSoupCharity.ipynb' Jupyter Notebook in this repository to recreate initial test study.
    - Model saved as 'AlphabetSoupCharity.h5'.
    - Model weights for every five epochs saved to following repository folder: 'Weights/Initial/'
* Optimized Test Study Files:
    - Use 'AlphabetSoupCharity_Optimization.ipynb' Jupyter Notebook in this repository to recreate optimized study.
    - Optimized model saved as 'AlphabetSoupCharity_Optimization.h5'.
    - Optimized model weights for every five epochs saved to following repository folder: 'Weights/Optimization/'

## Results

### Data Preprocessing
* Variable target: 'IS_SUCCESSFUL' binary classifier.
* Features included:
    - APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT
IS_SUCCESSFUL
What variable(s) should be removed from the input data because they are neither targets nor features?


* Dataset is scaled and dimensionality reduction applied using PCA, while preserving 90% of the explained variance. Dimensions are further reduced using t-SNE. The output is plotted for visual analysis, and a cluster analysis is performed with K-means.

## Analysis & Recommendation
* Visually, there appear to be two to three clusters, although they are not completely distinct. Suggested outlines as follows:

![Logistic Regression](Images/scatter_plot.png)

* Per the following elbow curve plotted using K-means cluster analysis, three clusters to the data are also suggested:

![Random Forest Classifier](Images/elbow_curve.png)

* Recommendation: This unsupervised learning model demonstrates that apparently three clusters exist in the dataset. For future analysis, use the "MYOPIC"--myopia diagnosis--feature of the dataset for labels/color on the scatter plot. Coloring by myopia diagnosis may show if there is tendency toward the condition amongst the three patient clusters observed. This added color analysis may support the suggestion that sub-categories of the patients exist which warrant separate predictor models.

## Source

* Reduced dataset from [Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute](https://clinicaltrials.gov/ct2/show/NCT00000169)

## Contact
E-mail: clawson131@gmail.com<br>
LinkedIn: https://www.linkedin.com/in/corey-lawson-enos/
