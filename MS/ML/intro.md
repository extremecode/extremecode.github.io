
https://learn.upgrad.com/course/2151/segment/18906/116804/354858/1844045

## Introduction to machine learning
* Regression: The output variable to be predicted is a continuous variable, e.g., predicting the score of a student in Class 12 based on their Class 10 marks.  
* Classification: The output variable to be predicted is a categorical variable, e.g., predicting whether a student will pass or fail Class 12 based on their Class 10 marks with the criteria being, let's say, a score over 40 being pass, otherwise fail. Here, we are classifying the person into a category, "fail" or "pass." 
* Clustering: No predefined notion of a label is allocated to the groups/clusters formed, e.g., based on their shopping history, customers are sent discount coupons for only one or more categories among clothing/appliances/accessories, so as to minimize effort and maximize profit.

It is often confusing to identify whether a machine learning algorithm is based on classification or clustering. They seem to be similar processes as both involve categorizing objects into one or more classes, but the notable difference is that classification already has predefined labels assigned to each input, whereas for clustering, these labels are not present, and objects are grouped on the basis of similarity and dissimilarity among them. 

Supervised learning methods: In this method, the model is built using past data with labels. Regression and classification algorithms fall under this category. The complete dataset is divided into training and testing data. The training data is used to teach the model a machine learning algorithm, and then, the model is tested on the fresh set of data or the test data. The output is given in the form of labels. The label could be a class label (classification model) or a continuous label (regression model). 

Unsupervised learning methods: Here, we do not have any predefined labels assigned to the past data. Instead, the model itself finds hidden patterns and insights from the given data. Clustering algorithms fall under this category. Data is grouped under different class labels on the basis of similarity or dissimilarity among them.

## Supervised and unsupervised learning methods
![image](https://user-images.githubusercontent.com/20191454/160465961-6ddfbd19-d40e-4a95-ab38-829c5e4652db.png)

## The linear regression model
![image](https://user-images.githubusercontent.com/20191454/160467040-96216462-4e2d-4837-8df3-7dc5ab7ccd43.png)
![image](https://user-images.githubusercontent.com/20191454/160467135-ca74bdd2-55d1-41ca-9456-3de75915e43c.png)
https://www.mathsisfun.com/equation_of_line.html
![image](https://user-images.githubusercontent.com/20191454/160469111-0024a2fb-4eed-4f3a-bee9-bbc2d72a91d3.png)


A simple linear regression model attempts to explain the relationship between a dependent variable and an independent one using a straight line.

The independent variable is also known as the predictor variable, and the dependent variables are known as the output variables.
![image](https://user-images.githubusercontent.com/20191454/160469697-48511590-3c11-4995-9d1e-e4f08f06b1a1.png)

![image](https://user-images.githubusercontent.com/20191454/160472322-21163d56-2137-4835-a4e5-ca437d8f4086.png)

![image](https://user-images.githubusercontent.com/20191454/160473420-2663f014-6cce-4be0-9a62-847e4f52ce1f.png)

```markdown

Machine learning models can be classified into the following categories:
Supervised learning method: Past data with labels is available to build the model.
Regression: The output variable is continuous in nature.
Classification: The output variable is categorical in nature.
Unsupervised learning method: Past data with labels is not available.
Clustering: There is no predefined notion of labels.
The past dataset is divided into two parts in the supervised learning method: 
Training data is used for the model to learn from during modeling.
Testing data is used by the trained model for prediction and model evaluation.
Linear regression models can be classified into two types depending upon the number of independent variables: 
Simple linear regression: This is used when the number of independent variables is 1.
Multiple linear regression: This is used when the number of independent variables is more than 1.
The equation of the best-fit regression line 
Y
=
β
0
+
β
1
X
 can be found by minimizing the cost function (RSS in this case, using the ordinary least squares method), which is done using the following two methods:
Differentiation
Gradient descent 
The strength of a linear regression model is mainly explained by R², where R² = 1 - (RSS/TSS).
RSS: Residual sum of squares
TSS: Total sum of square
RSE helps in measuring the lack of fit of a model on a given dataset. The closeness of the estimated regression coefficients to the true ones can be estimated using RSE. It is related to RSS by the formula: 
R
S
E
=
√
R
S
S
d
f
, where 
d
f
=
n
−
2
 and 
n
 is the number of data points.
```
https://online.stat.psu.edu/stat462/node/98/

## Residuals

## Residual sum of squares (RSS) and R² (R-squared)







