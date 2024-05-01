# hypotheses-test
codes of hypotheses test
import numpy as np
from scipy.stats import chi2_contingency

# Create the contingency table
observed = np.array([[50, 70],
                     [80, 100],
                     [60, 90],
                     [30, 50],
                     [20, 50]])

# Perform chi-square test
chi2, p, dof, expected = chi2_contingency(observed)

print("Chi-Square Statistic:", chi2)
print("p-value:", p)
print("Degrees of Freedom:", dof)
print("Expected frequencies:\n", expected)

from scipy.stats import chi2
#### critical value
# Significance level
alpha = 0.05

# Degrees of freedom
df = 4

# Find the critical value
critical_value = chi2.ppf(1 - alpha, df)

print("Critical Value:", critical_value)
# test statistic
import math

# Given values
x_bar = 3050  # sample mean weekly cost
mu = 1000 + 5 * 600  # theoretical mean weekly cost
sigma = 5 * 25  # standard deviation
n = 25  # sample size

# Calculate the test statistic
t = (x_bar - mu) / (sigma / math.sqrt(n))

print("Test Statistic (t):", t)

# test statistic
from scipy.stats import norm

# Alpha level
alpha = 0.05

# Determine the critical value
critical_value = norm.ppf(1 - alpha/2)  # Dividing alpha by 2 for a two-tailed test

print("Critical Value from standard normal distribution table:", critical_value)
