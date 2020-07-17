# Pump it Up: Data Mining the Water Table
 Mulilabel classification of water wells competition<br/>
 [Competition Web Page](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/23/)
 
 ##### Competition Summary:<br/>
  Using data from Taarifa and the Tanzanian Ministry of Water, can you predict which pumps are functional, which need some repairs, and which don't work at all? 
  This is an intermediate-level practice competition. Predict one of these three classes based on a number of variables 
  about what kind of pump is operating, when it was installed, and how it is managed. A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.
 
 ##### Approach Sumamry: 
 Cleaned data looking at the ratio of Functional : Needs Repair : Non Functional <br/>
 I looked for insights or relevant data that had ratios that were different than population as a whole to derive insight from them as to why they were different. <br/>
 
 I used the XGBClassifier algorithm to train the model.
 
 #### Relevant Files in the Repository
 [Current - Data Cleaning and EDA Notebook](https://github.com/bsamaha/Competition---DrivenData---Pump-It-Up/blob/master/Iteration%202%20-%20Notebooks/Current%20-%20Data%20Cleaning%20and%20EDA%20Notebook.ipynb) - This notebook is where the data cleaning and exploration took place. 
 You can see in the notes in each section what methods were performed in different iterations. This notebook was a cleaned 
 up version of the iteration 1 notebooks.
 
 [Current - Multilabel Classifier Training Model](https://github.com/bsamaha/Competition---DrivenData---Pump-It-Up/blob/master/Iteration%202%20-%20Notebooks/Current%20-%20Multilabel%20Classifier%20Training%20Model.ipynb) - This notebook is a cleaned up version of the first modeling notebook. This is the most
 up to date notebook and all cleaned data from the Data Cleaning and EDA notebook is read in this notebook to turn into a model and 
 competition submission.
 
 [Models](https://github.com/bsamaha/Competition---DrivenData---Pump-It-Up/tree/master/Iteration%202%20-%20Notebooks/Models) - This is a list of generated models. The first number is the score it received. If the score i
 is negative it is a negative log loss score and if the score is positive it is the models accuracy. The iteration number does not correspond directly to the notebooks as the way I formatted was hard to keep up.
 #### Future Work 
 1. Impute missing data for missing data in lat and long.
 2. Try to perform 2 binary label classifcations instead of 1 multilabel to see if it could improve accuracy.
 3. Use a KNN or some other technique to clearly define clusters of the imbalanced class 'functional_needs_repair'

##### Visualization of the Data
![Data Viz](https://github.com/bsamaha/Competition---DrivenData---Pump-It-Up/blob/master/Iteration%202%20-%20Notebooks/Visualizations/Well_Status_Map_with_outliers.html)