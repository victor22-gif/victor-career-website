Simple Mann-Whitney U Test

Overview

This Jupyter notebook demonstrates how to perform the Mann-Whitney U Test, a non-parametric test used to assess whether two independent groups have different distributions. It is commonly used when the assumption of normality is not met for the data. The test evaluates if the distributions of two groups are significantly different, based on their rank sums.

Files

Simple_Mann_whitney_test.ipynb: The main Jupyter notebook for performing the test.

Simple_Mann_whitney_test.ipynb_: Backup or duplicate of the main notebook.


Steps Involved

1. Data Preparation: The notebook uses example data for two independent groups, group_A and group_B, each containing five observations.


2. Mann-Whitney U Test: Using scipy.stats.mannwhitneyu(), we compute the U-statistic and p-value to test if there is a significant difference between the two groups.


3. Result Interpretation: Based on the p-value, the notebook interprets whether the difference between the groups is statistically significant (p-value < 0.05) or not (p-value >= 0.05).



Code Explanation

import scipy.stats as stats

# Example data for two independent groups
group_A = [23, 21, 17, 32, 45]
group_B = [29, 31, 39, 22, 26]

# Perform Mann-Whitney U Test
stat, p_value = stats.mannwhitneyu(group_A, group_B)

# Output the results
print(f"U-statistic: {stat}")
print(f"P-value: {p_value}")

# Interpretation
if p_value < 0.05:
    print("There is a significant difference between the groups.")
else:
    print("There is no significant difference between the groups.")

Example Output:

U-statistic: 10.0
P-value: 0.6904761904761905
There is no significant difference between the groups.

Key Concepts

U-statistic: The test statistic for the Mann-Whitney U test, representing the difference between the ranks of the two groups.

P-value: A measure of the strength of evidence against the null hypothesis. A value less than 0.05 typically indicates a significant difference.

Interpretation: The notebook includes logic to interpret whether the observed difference between the groups is statistically significant based on the p-value.


Requirements

Python 3.x

Libraries: scipy (for statistical analysis)


To run the notebook, you will need a Jupyter environment or any Python IDE that supports Jupyter Notebooks.

Usage

1. Open Simple_Mann_whitney_test.ipynb in Jupyter or Google Colab.


2. Modify the input data (group_A and group_B) to test with your own dataset.


3. Run the notebook to compute the U-statistic and p-value, and interpret the results.



Conclusion

This notebook serves as a basic introduction to conducting the Mann-Whitney U test using Python. You can extend the code to work with your datasets, modify it to handle larger or more complex data, or adapt it for use in real-world analysis tasks.


