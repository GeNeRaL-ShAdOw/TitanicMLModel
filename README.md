<h1>Supervised Machine Learning Model on Titanic Dataset</h1>
<br>
<div align=center>
  <img src="https://i.imgur.com/676V8TM.jpg" alt=titanic/>
</div>
<h3>About the project</h3>
<br>
<p> This project is a completely isolated project for hands down practice on data science.The project is used on a dataset which contains about 1,300 entries.The objective of this model is to determine the 'survived' status for each passenger, either 0(failed to survive) or 1(survived).</p>
<br>
<hr size="3" nospace>
<h3>Dataset</h3>
<p>The dataset was provided by <a href="https://www.kaggle.com/datasets/hesh97/titanicdataset-traincsv">Kaggle</a> (click to follow), and falls under a small dataset with around 1,300 entries. There are 12 attributes in the raw data, out of which Survived is the independent one, and contains some unfilled date which needs to be filled. The survived column contains either a 0 or a 1, determining the status of the passenger.</p>
<br>
<hr size="3" nospace>
<h3>Importing Dataset</h3>
<p>The dataset is downloaded and imported as a csv file. In this case, we have two datasets already split into test and train and we will work on them parallely.</p>
<hr size="3" nospace>
<h3>Data cleaning</h3>
<p>Data Cleaning consists of many steps which are absolutely required for high presicion,low error model deployment. 
These are:</p>
<ul>
 <li>Dealing with null values.</li>
 <li>Checking for (Quasi)Constant values.</li>
 <li>Checking and deleting duplicate data.</li>
</ul>
<hr size="3" nospace>
<h3>EDA</h3>
<p>Exploratory Data Analysis is done usually to make the data present more pleasing to present, or more understanding. EDA is useful for creating associations between variables, and can help us determine feature selection in the long run.</p>
<img src="https://i.imgur.com/yQmqiE6.png" alt="Factorplot"/>
<hr size="3" nospace>
<h3>Data Preprocessing</h3>
<p>Data Preprocessing is a process with which when combined with data cleaning gives up with clean dataset, which can be used for predictions and classifications. Data Preprocessing can have feature selection, which is apparently of high importance while using classifiers to determine the independent variable. It also contains label encoding, which is just converting string data to numbers which the computer can understand and work with.</p>
<hr size="3" nospace>
<h3>Applying ML models</h3>
<p>After the data has been split, we need to finally start applying our classifiers.The classifiers we used in this project are:</p>
<ul>
  <li>Logistic Regression.</li>
  <li>SVC.</li>
  <li>K-nearest Neighbour.</li>
  <li>Decision Tree Regressor.</li>
  <li>Random Forest Regressor.</li>
  <li>XGBoost Regressor.</li>
  <li>Naive Bayes Regressor.</li>
</ul>
<br>
<h4>XGBoost Regressor was chosen since the mean squared error was minimum and accuracy was maximum.</h4>
<hr size="3" nospace>
<h3>Evaluation/Performance matrix</h3>
<p>If we talk about classification problems, the most common metrics used are:
<ul>
  <li>Accuracy</li>
  <li>Precision (P)</li>
  <li>Recall (R)</li>
  <li>F1 score (F1)</li>
</ul>
Area under the ROC (Receiver Operating Characteristic) curve or simply AUC (AUC):

If we calculate the area under the ROC curve, we are calculating another metric which is used very often when you have a dataset which has skewed binary targets. This metric is known as the Area Under ROC Curve or Area Under Curve or just simply AUC. There are many ways to calculate the area under the ROC curve
AUC is a widely used metric for skewed binary classification tasks in the industry,and a metric everyone should know about
Log loss

Log Loss = - 1.0 ( target log(prediction) + (1 - target) * log(1 - prediction) )

We can calculate precision and recall for each class in a multi-class classification problem:
Micro averaged precision: calculate precision for all classes individually and then average them
Micro averaged precision: calculate class wise true positive and false positive and then use that to calculate overall precision
Weighted precision: same as macro but in this case, it is weighted average depending on the number of items in each class
</p>
<hr size="3" nospace>
<h3>Deployment</h3>
<p>After the model has ben applied, a quick backup of the pre-processed data is made, and the classifer is worked upon the dataset. The changed dataset is then given to the user and is exported to storage.</p>
