# Pearson-Correlation

Let's say we have a dataset with four columns:

![Uploading Screenshot 2024-07-05 at 20.33.58.png…]()

We want to determine if there is a relationship between study hours and scores. Since both study hours and scores are continuous variables, we can examine their correlation. In this explanation, we will use linear regression  (Pearson correlation) methods to investigate this relationship. 

Actually, the method that measures the strength and direction of the linear relationship between two continuous variables is the Pearson correlation. However, since Pearson correlation and linear regression share a conceptual basis in understanding linear relationships between variables. it is also correct to refer to linear regression in this context. The formula to calculate the correlation between two continuous features is:

![Uploading Screenshot 2024-07-05 at 17.01.10.png…]()

That formula returns value from -1 untill 1, where :

•	r = 1 indicates a perfect positive linear relationship.
•	r = −1 indicates a perfect negative linear relationship.
•	r = 0 indicates no linear relationship.

We will implement the Pearson correlation both manually (by hand) and using Python.
