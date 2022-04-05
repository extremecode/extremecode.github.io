# Multple Linear Regression

![image](https://user-images.githubusercontent.com/20191454/161699640-e1dcb3ce-b964-45a9-bdcf-72185d9bed43.png)
![image](https://user-images.githubusercontent.com/20191454/161790223-ac0f6908-1c64-42a4-814e-1213849b93d3.png)
![image](https://user-images.githubusercontent.com/20191454/161791077-07e574de-73b2-45bd-a7dc-5999665546e7.png)
![image](https://user-images.githubusercontent.com/20191454/161791161-90f189d6-eebc-4b77-bb5f-e37b05fc0c3c.png)
![image](https://user-images.githubusercontent.com/20191454/161792266-2bd4fc4c-c868-4ec9-839e-922ad44e13ea.png)
![image](https://user-images.githubusercontent.com/20191454/161794238-828b0944-637a-4508-96e6-c62c3ab078f9.png)
![image](https://user-images.githubusercontent.com/20191454/161796939-63f9ac33-f142-4941-9082-9de1dc86cabd.png)
![image](https://user-images.githubusercontent.com/20191454/161799838-f66e0ed6-c103-40da-aaf0-1a756f14922c.png)
https://stats.idre.ucla.edu/other/mult-pkg/faq/general/faqwhat-is-dummy-coding/
https://stats.stackexchange.com/questions/89533/convert-a-categorical-variable-to-a-numerical-variable-prior-to-regression
https://stackoverflow.com/questions/32108179/linear-regression-normalization-vs-standardization
https://en.wikipedia.org/wiki/Feature_scaling
![image](https://user-images.githubusercontent.com/20191454/161800951-f9d8db71-89a5-430c-bd15-9ea1f7169f15.png)
![image](https://user-images.githubusercontent.com/20191454/161801792-3901418a-44cd-4daf-82a2-84cff6e64cdb.png)
https://en.wikipedia.org/wiki/Akaike_information_criterion
https://en.wikipedia.org/wiki/Bayesian_information_criterion
https://en.wikipedia.org/wiki/Mallows%27s_Cp
https://faculty.math.illinois.edu/~hildebr/213/inductionsampler.pdf
![image](https://user-images.githubusercontent.com/20191454/161802380-1e34c5dc-0f8d-43ed-8b9f-07efaeb2e7e9.png)
![image](https://user-images.githubusercontent.com/20191454/161802654-a0e85cce-c965-4a4e-9be9-70753d648ca0.png)
![image](https://user-images.githubusercontent.com/20191454/161803632-5cb1fb66-87e6-4e86-a8ba-c4587491f607.png)
http://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFE.html
Recursive feature elimination is based on the idea of repeatedly constructing a model (for example, an SVM or a regression model) and choosing either the best or the worst performing feature (for example, based on coefficients), setting the feature aside and then repeating the process with the rest of the features. This process is applied until all the features in the data set are exhausted. Features are then ranked according to when they were eliminated. As such, it is a greedy optimisation for finding the best performing subset of features.
http://blog.datadive.net/selecting-good-features-part-iv-stability-selection-rfe-and-everything-side-by-side/
```markdown
Here is a summary of what you learned in this session:

One variable might not be enough
When many variance values are not explained by just one feature
When predictions are inaccurate
Formulation of MLR
Additional considerations when building a model using MLR instead of SLR
Overfitting
Multicollinearity
Feature selection
Dealing with categorical variables
Dummy variables for fewer levels
Feature scaling
Standardization
MinMax scaling
Scaling for categorical variables
Model assessment and comparison
Adjusted R-squared
AIC, BIC
Feature selection
Manual feature selection
Automated feature selection
Finding a balance between two manual feature selection and automated feature selection
 

Linear regression is used in various fields such as real estate, telecom, e-commerce, etc. to build predictive models. Let's look at one such example from the real estate industry. Here, you will predict the price of a house on the basis of some predictor variables, such as floor area, number of bedrooms, parking space, etc.

Problem Statement
Consider that a real estate company has data about real estate prices in Delhi. The company wants to optimize the selling price of its properties, based on important factors such as area, bedrooms, parking, etc.

 

Essentially, the company wants:

To identify the variables affecting house prices, e.g., area, number of rooms, bathrooms, etc.
To create a linear model that quantitatively relates house prices with variables, such as the number of rooms, area, number of bathrooms, etc.
To know the accuracy of the model, i.e., how well these variables predict house prices





```


![image](https://user-images.githubusercontent.com/20191454/161813061-c6ac4ecd-39aa-4958-82e6-5c6f3e0b150f.png)
![image](https://user-images.githubusercontent.com/20191454/161814368-532e5937-b7ad-42cf-8b90-5286c05d04de.png)
![image](https://user-images.githubusercontent.com/20191454/161816359-72a981da-6107-45e7-8292-a120e0b721e9.png)

![image](https://user-images.githubusercontent.com/20191454/161820427-41ac613d-d634-47ce-9ce9-6b434de6639c.png)
![image](https://user-images.githubusercontent.com/20191454/161820495-bd7993bc-c069-41d0-85e0-26c3bd8e0605.png)
![image](https://user-images.githubusercontent.com/20191454/161821218-0771e2a5-c919-423f-9889-8397c72895cc.png)
![image](https://user-images.githubusercontent.com/20191454/161822287-5486f154-a397-4d32-9b2d-8bdbe025d530.png)
![image](https://user-images.githubusercontent.com/20191454/161822890-01efb84f-471c-45e6-8ccc-f6237b1797ae.png)

![image](https://user-images.githubusercontent.com/20191454/161823326-2932ffb8-3a75-4bcb-98d3-55ded9a69a51.png)

always drop one by one 
Now that you seem to have a fair model, in the next segment, let's perform the final step of building your model: analyze the residual terms and predict the price.

check RSS
![image](https://user-images.githubusercontent.com/20191454/161824221-c216ad72-d700-4c90-b283-c2f8e37ee531.png)


![image](https://user-images.githubusercontent.com/20191454/161824398-42c91ab9-dacf-48e1-8860-9dfedc8c497b.png)

![Uploading image.png…]()

