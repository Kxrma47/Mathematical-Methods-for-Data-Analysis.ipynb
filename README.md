# Mathematical Methods for Data Analysis 

## Overview

This document provides a summary and analysis of various computational tasks related to mathematical methods for data analysis. The tasks cover fundamental Python programming, NumPy operations, and data analysis using Pandas and visualization libraries. Each task is designed to apply specific concepts and techniques essential for data analysis and machine learning.

---

## Table of Contents

1. [Python Basics](#python-basics)
   - Task 1: Generating a Geometric Progression
   - Task 2: Palindrome Number Checker
   - Task 3: Finding Palindromes Starting from 1000
   - Task 4: Finding the Minimum of Three Numbers
2. [NumPy Exercises](#numpy-exercises)
   - Task 1: Creating a Random Array with Specific Sum
   - Task 2: Calculating Distances Between Arrays
   - Task 3: Transforming Array Values
   - Task 4: Extracting a Column with the Maximum Element
   - Task 5: Replacing Missing Values with Median
   - Task 6: Computing Mean Values for Image Channels
   - Task 7: Extracting Unique Vertical Layers from a 3D Matrix
3. [Pandas and Visualization](#pandas-and-visualization)
   - Task 1: Exploratory Data Analysis on Titanic Dataset
   - Task 2: Visualizing Age Distribution
   - Task 3: Analyzing Passenger Titles
   - Task 4: Correlation Between Class and Fare
   - Task 5: Fare Distribution by Embarkation Port
   - Task 6: Age Distribution by Survival Status and Gender
4. [Conclusion](#conclusion)

---

## Python Basics

### Task 1: Generating a Geometric Progression

**Purpose**: To generate the first N terms of a geometric progression with a given first term `a` and common ratio `r`, without directly using the formula for the product.

**Analysis**:

- Utilize the relation \( a_n = a \times r^n \) to compute each term.
- Use NumPy functions to create an array of exponents from 0 to N-1.
- Multiply the initial term `a` by `r` raised to the power of the exponents array.

**Outcome**: Successfully generated the first N terms of the geometric progression.

---

### Task 2: Palindrome Number Checker

**Purpose**: To check whether a given integer `N` is a palindrome, meaning it reads the same forwards and backwards.

**Analysis**:

- Convert the integer to a string.
- Compare the string to its reverse using slicing.
- Return `True` if the number is a palindrome, `False` otherwise.

**Outcome**: Correctly identified palindrome and non-palindrome numbers in the provided test cases.

---

### Task 3: Finding Palindromes Starting from 1000

**Purpose**: To find the first N palindrome numbers starting from 1000.

**Analysis**:

- Utilize the palindrome checker function from Task 2.
- Iterate over numbers starting from 1000.
- Collect numbers that are palindromes until N palindromes are found.

**Outcome**: Successfully found and listed the first N palindromes starting from 1000.

---

### Task 4: Finding the Minimum of Three Numbers

**Purpose**: To find the minimum of three numbers `a`, `b`, and `c` without using built-in functions like `min` or `max`.

**Analysis**:

- Use conditional statements to compare the numbers.
- First, compare `a` and `b`, store the smaller value.
- Then, compare the result with `c`, update if `c` is smaller.

**Outcome**: Correctly determined the minimum of three numbers across multiple test cases.

---

## NumPy Exercises

### Task 1: Creating a Random Array with Specific Sum

**Purpose**: To create a random array of length 17 where the sum of its elements equals 6.

**Analysis**:

- Generate a random array using `np.random.rand(17)`.
- Calculate the sum of the array.
- Scale the array by multiplying each element by \( \frac{6}{\text{sum of the array}} \) to adjust the total sum to 6.

**Outcome**: Produced an array of length 17 with a total sum of 6.

---

### Task 2: Calculating Distances Between Arrays

**Purpose**: To compute various distances between two random arrays `a` and `b` without using specialized functions.

**Analysis**:

- **Manhattan Distance**: \( d = \sum_i |a_i - b_i| \)
- **Euclidean Distance**: \( d = \sqrt{\sum_i (a_i - b_i)^2} \)
- **Chebyshev Distance**: \( d = \max_i |a_i - b_i| \)
- **Cosine Distance**: \( d = 1 - \frac{a \cdot b}{\|a\| \|b\|} \)
- Implement each formula using basic NumPy operations.

**Outcome**: Successfully calculated and reported the distances.

---

### Task 3: Transforming Array Values

**Purpose**: To transform a random integer array so that:

- Maximum element(s) become -1.
- Minimum element(s) become -4.
- Other elements are scaled to be within (-4, -1), preserving order.

**Analysis**:

- Identify the maximum and minimum values in the array.
- Replace maximum values with -1 and minimum values with -4.
- Linearly scale the remaining values between -4 and -1.

**Outcome**: Transformed the array according to the specified criteria.

---

### Task 4: Extracting a Column with the Maximum Element

**Purpose**: To create an 8×5 array with integers from -7 to 43 and extract the column containing the maximum element.

**Analysis**:

- Generate the array using `np.random.randint(-7, 44, size=(8, 5))`.
- Locate the index of the maximum element using `np.argmax` and `np.unravel_index`.
- Extract the column corresponding to the maximum element's column index.

**Outcome**: Successfully extracted and displayed the desired column.

---

### Task 5: Replacing Missing Values with Median

**Purpose**: To replace all missing (NaN) values in an array with the median of the non-missing values.

**Analysis**:

- Use `np.nanmedian` to compute the median while ignoring NaNs.
- Identify NaN positions using `np.isnan`.
- Replace NaNs with the computed median.

**Outcome**: All missing values were replaced, resulting in an array without NaNs.

---

### Task 6: Computing Mean Values for Image Channels

**Purpose**: To compute the mean values for each of the three color channels in an image represented as a 3D NumPy array of shape (n, m, 3).

**Analysis**:

- Use `np.mean` over the first two axes (height and width).
- This computes the mean for each channel across all pixels.

**Outcome**: Obtained a vector containing the mean of each channel.

---

### Task 7: Extracting Unique Vertical Layers from a 3D Matrix

**Purpose**: To extract all unique vertical layers (along the first axis) from a 3D matrix.

**Analysis**:

- Reshape the 3D matrix to a 2D array where each row represents a layer.
- Use `np.unique` with `axis=0` to find unique layers.
- Retrieve and reshape the unique layers back to their original dimensions.

**Outcome**: Extracted and presented the unique vertical layers from the matrix.

---

## Pandas and Visualization

### Task 1: Exploratory Data Analysis on Titanic Dataset

**Purpose**: To perform initial data exploration on the Titanic dataset by answering specific questions.

**Analysis and Findings**:

1. **Missing Values**:
   - Columns with missing data: `Age` (177), `Cabin` (687), `Embarked` (2).

2. **Survival Rate**:
   - 38.38% of passengers survived.
   - Classes are imbalanced, with more passengers not surviving (61.62%).

3. **Gender Distribution**:
   - Males: 577 passengers.
   - Females: 314 passengers.

4. **Least Popular Embarkation Port**:
   - Queenstown (Q) was the least popular.

5. **Passenger Classes**:
   - There were 3 classes: 1st, 2nd, and 3rd.

6. **Average Ticket Fare**:
   - Overall average fare: $32.20.
   - Average fare by class:
     - 1st Class: $84.15
     - 2nd Class: $20.66
     - 3rd Class: $13.68

**Outcome**: Gained insights into the dataset's structure, missing values, and key statistics.

---

### Task 2: Visualizing Age Distribution

**Purpose**: To visualize the age distribution of passengers and analyze it based on minimum, maximum, and mean ages, including differences between genders.

**Analysis**:

- **Age Statistics**:
  - Minimum age: 0.42 years.
  - Maximum age: 80 years.
  - Overall mean age: 29.70 years.
  - Mean age of males: 30.73 years.
  - Mean age of females: 27.92 years.

- **Visualizations**:
  - Histogram of age distribution with lines indicating min, max, and mean ages.
  - Separate mean lines for males and females.

**Conclusions**:

- Majority of passengers were between 20 and 40 years old.
- The dataset includes infants and elderly passengers.
- Males were slightly older on average compared to females.

---

### Task 3: Analyzing Passenger Titles

**Purpose**: To extract titles from passenger names and analyze their frequency and distribution by gender.

**Analysis**:

- Extracted titles using string manipulation.
- **Unique Titles**: Identified 16 unique titles.
- **Title Counts**: Counted the number of passengers for each title.
- **Most Popular Titles**:
  - Male: "Mr." with 517 passengers.
  - Female: "Miss." with 182 passengers.

**Outcome**: Provided insights into the social status and demographics of passengers based on their titles.

---

### Task 4: Correlation Between Class and Fare

**Purpose**: To determine the correlation between passenger class and ticket fare, and to visualize fare distribution by embarkation port.

**Analysis**:

- **Correlation Coefficient**: Calculated a Pearson correlation of -0.5495 between `Pclass` and `Fare`.
- **Interpretation**: Negative correlation indicates that higher classes (lower `Pclass` value) are associated with higher fares.
- **Mean Fare by Port**:
  - Cherbourg (C): $59.95
  - Queenstown (Q): $13.28
  - Southampton (S): $27.08
- **Visualizations**:
  - Scatter plot with regression line showing the negative correlation.
  - Violin plots displaying fare distributions for each embarkation port.

**Conclusions**:

- Passengers in higher classes paid more for their tickets.
- Cherbourg had higher average fares, suggesting more first-class passengers embarked there.
- Queenstown had lower fares, indicating a predominance of third-class passengers.

---

### Task 5: Fare Distribution by Embarkation Port

**Purpose**: To analyze how embarkation port relates to ticket prices.

**Analysis**:

- Created box plots, violin plots, and strip plots to visualize fare distributions.
- **Findings**:
  - **Cherbourg (C)**: Higher median fares and greater variability; associated with wealthier passengers.
  - **Southampton (S)**: Moderate fares with a wider range; mixed passenger classes.
  - **Queenstown (Q)**: Lower fares; predominantly third-class passengers.

**Conclusions**:

- The embarkation port is indicative of the socio-economic status of passengers.
- Visualizations highlight significant differences in fare distributions among the ports.

---

### Task 6: Age Distribution by Survival Status and Gender

**Purpose**: To visualize and compare the age distribution of passengers based on survival status and gender.

**Analysis**:

- **Age Distribution by Survival**:
  - Plotted histograms for survived and not survived passengers.
  - Mean age of survivors: 28.34 years.
  - Mean age of non-survivors: 30.63 years.

- **Age Distribution by Gender**:
  - Plotted histograms for males and females.
  - Mean age of males: 30.73 years.
  - Mean age of females: 27.92 years.

**Conclusions**:

- Younger passengers had a higher survival rate.
- Females were generally younger than males.
- Age and gender were significant factors in survival, possibly due to evacuation protocols prioritizing women and children.

---

## Conclusion

The tasks covered in this assignment provided practical experience with fundamental concepts in data analysis:

- **Python Programming**: Implementing algorithms without relying on built-in functions enhances understanding of underlying processes.
- **NumPy Operations**: Utilizing NumPy for efficient array manipulations is crucial for handling large datasets.
- **Data Exploration with Pandas**: Extracting meaningful insights from data requires familiarity with data structures and descriptive statistics.
- **Data Visualization**: Effective visualization techniques are essential for interpreting data patterns and communicating findings.
- **Statistical Analysis**: Understanding correlations and distributions aids in uncovering relationships within data.
