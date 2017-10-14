In this repository I have used some machine learning techiniques to predict that mushroom is poisonous or not usig the training data set (mushroon_test.csv) and the models are then performed on test data set (mushroom_test.csv). And the final prediction is stored in file mushroom_predict.csv

for more detail about problem statement read 'Problem Statement.docx' and 'Data Description.docx'

My basic approach that I have used in the ipython notebook
1. I have done some basic EDA and then found that:-
	a. There was only one type of categorical variable in the column viel-type. So it had high correlation with the other variables in the train data set and also due to same varible in whole column the variable can not be used to predict any results. 
	b. There was only two continious variable in the data set and rest are the categorical variables
2. After that I encoded all the categorical variables by using label encoding function of sklearn 
3. There was a missing value in stalk-root which was written in the form of string('?') and contribute around 30% of that column so we can not delete that directly. to solve this issue i considered '?' as a type of categorical variable and considered that as a type of variable in features to predict the results 
4. Then plotted some graph and heamaps to get the more idea about the data and to look into any type of results form the data. folloeing are the results that i got from the graph:
	a. All the mushrooms of odour of type 0&3 are all edible and the musroom of odor type 5 contains a small fraction of poisonous mushrooms
	b. The graph of stalk-color-above-ring and stalk-color-below-ring are quite similar and also of stalk-surface above the ring and stalk-surface-below the ring 

5. Then I used some machine learning models like:
	a. KNN 
	b. Logistic Regression
	c. Decision Tree 
	d. Random Forest 
	Ater that I also used boosting methodd like:
	a. AdaBoosting 
	b. Gradient Boosting 
6. After that I predicted my results using AdaBoost Classifier to get the final answers on test data 
7. final solution of predicted results in saved as mushroom_predict.csv
