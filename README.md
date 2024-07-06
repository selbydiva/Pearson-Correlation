# Pearson Correlation: Assessing Correlation Between Two Continuous Variables

Let's say we have a dataset with four columns:

<img width="1153" alt="Screenshot 2024-07-05 at 20 33 58" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/2afd490c-8667-44c0-8fe2-5d87a2d84011">


We want to determine if there is a relationship between study hours and scores. Since both study hours and scores are continuous variables, we can examine their correlation. In this explanation, we will use linear regression  (Pearson correlation) methods to investigate this relationship. 

Actually, the method that measures the strength and direction of the linear relationship between two continuous variables is the Pearson correlation. However, since Pearson correlation and linear regression share a conceptual basis in understanding linear relationships between variables, it is also correct to refer to linear regression in this context. The formula to calculate the correlation between two continuous features is:

<img width="1437" alt="2-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/517da252-8b3b-4eec-8251-5188ab272279">

That formula returns value from -1 untill 1, where :

•	r = 1 indicates a perfect positive linear relationship.<br>
•	r = −1 indicates a perfect negative linear relationship.<br>
•	r = 0 indicates no linear relationship.

We will implement the Pearson correlation both manually (by hand) and using Python.

# Manually (By Hand)

When calculating Pearson correlation manually, it's beneficial to use a table to simplify the process. As shown, each component of the Pearson correlation coefficient (r) formula is computed first, resulting in an r value of 0.8154.

<img width="1061" alt="3-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/8cb4238e-b807-417a-b42b-979305e753e0">


This indicates a strong relationship between the variables "study hours" and "score". To confirm the validity of this relationship and there’s no influence of random chance, particularly with smaller datasets, conducting a statistical significance using t-test is recommended. The following is the calculation of t-statistics for determining statistical significance of Pearson correlation coefficient:



<img width="1437" alt="4-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/4f93aa38-9c78-4d50-86c6-7930a04aaeea">

<img width="1438" alt="5-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/e8560747-604a-42dd-b8e3-dc423fd2c7e0">


To determine the significance of the relationship between the variables (study hours and score), we compare the t-statistic value to the critical t-value:

•	If the t-statistic is greater than the critical t-value, there is a significant relationship between the variables.<br>
•	If the t-statistic is less than or equal to the critical t-value, there is no significant relationship between the variables.<br>

To find the critical t-value, we use a t-distribution table with degrees of freedom equal to 5 (calculated as N−2), and a significance level of 0.05.


<img width="1432" alt="6-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/0e5b55c2-1ae8-4c38-94e2-2e5b47945ee2">

<img width="1438" alt="7-pcc" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/9a3fbb84-4e11-429c-8c72-167fe0681990">


Based on the t-table, the critical t-value is 2.571, which is less than the t-statistic. Therefore, there is a significant relationship between the variables of study hours and score.

# Using Python

You can easily calculate the Pearson correlation coefficient (PCC) and assess its statistical significance in Python using the `pearsonr` function from the `scipy.stats` library.

<img width="1035" alt="Python" src="https://github.com/selbydiva/Pearson-Correlation/assets/154320650/95574ee9-c29f-4995-b856-f576734ba807">

Using this library, you can simultaneously find the Pearson correlation coefficient and its statistical significance. The resulting Pearson correlation coefficient matches the one obtained from manual calculations.

In manual calculations, statistical significance is determined by comparing the t-statistic to the critical t-value. With this library, statistical significance is found by comparing the p-value to the significance level. Both methods can be used to assess statistical significance.










