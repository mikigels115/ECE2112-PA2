# ECE-2112-PA-2
Made by: Mike Angelo P. Atienza | Section: 2ECE-B

This repository contains the Programming Assignment 2 for our course "Advanced Computer Programming and Algorithms" this S.Y. 2026-2027. This project contains three python programming problems focusing on NumPy arrays.

# 1. REPRODUCIBLE NORMALIZATION PROBLEM
Create a reproducible random 5 × 5 integer ndarray named X. The following statements will be used:

```
np.random.seed(2112)

X = np.random.randint(10, 101, size=(5, 5))
```

The formula for the normalized array is   

**Z = (X - x̄) / σ**,

where x̄ is the mean of all 25 elements and σ is the population standard deviation as returned by
NumPy’s default std() call. Store the normalized array in X normalized.

**Functions and methods that were used here:** 

* **(`import numpy as np`):** It is used to load NumPy libraries.
* **(`np.random.seed()`):** Fixes the random number generator so it can produce the exact same sequence of numbers every time the code runs.
* **(`np.random.randint()`):** Generates a 5 x 5 matrix filled with random integers ranging from 10 up to 100. 
* **(`np.mean()`):** The mean for the given equation "normalized array".
* **(`np.std()`):** The standard deviation for the given equation "normalized array".
* **(`X_normalized`):** The normalized array.
* **(`np.save("X_normalized.npy", X_normalized)`):** It saves a single NumPy array "X_normalized" into the computer in a binary file called "X_normalized.npy".
```
import numpy as np
np.random.seed(2112)

X = np.random.randint(10, 101, size=(5, 5))
print(X)

Mean = np.mean(X)
print(Mean)

Standard_Deviation = np.std(X)
print(Standard_Deviation)

X_normalized = (X - Mean) / Standard_Deviation
print(np.mean(X_normalized))  
print(np.std(X_normalized))

np.save("X_normalized.npy", X_normalized)
```

# 2. CUBES DIVISIBLE BY 4 PROBLEM
Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C. Also, C starts from 1^3 and ends to 100^3. To obtain every cubed value divisible by 4, use a Boolean condition on C. Store the selected values in div_by_4. Preserve NumPy’s normal row-major selection order.

**Functions and methods that were used here:** 

* **(`import numpy as np`):** It is used to load NumPy libraries.
* **(`np.arange()`):** It is to obtain integers starting from 1 to 100 of the array.
* **(`C**3`):** The cubed value of all integers starting from 1 to 100 of the array.
* **(`np.reshape()`):** It reshapes the array into the desired shape of 10 x 10 ndarray.
* **(`print(np.shape(C))`):** The 10 x 10 ndarray.
* **(`C[C % 4 == 0]`):** The Boolean Condition on C.
* **(`print(len(div_by_4))`):** The length of elements stored in div_by_4.
* **(`np.save("div_by_4.npy", div_by_4)`):** It saves a single NumPy array "div_by_4" into the computer in a binary file called "div_by_4.npy".

```
C = np.arange(1,101,1)

C = C**3

C = np.reshape(C,(10,10))
print(C)

print(np.shape(C))

div_by_4 = C[C % 4 == 0]
print(div_by_4)

print(len(div_by_4))

np.save("div_by_4.npy", div_by_4)
```



# 3. ABOVE-MEAN SQUARES PROBLEM
Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing
row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean
filtering to select only the elements strictly greater than S mean. Store these values in above mean


**Functions and methods that were used here:** 

* **(`import numpy as np`):** It is used to load NumPy libraries.
* **(`np.arange()`):** It is to obtain integers starting from 1 to 36 of the array.
* **(`S**2`):** The squared value of all integers starting from 1 to 36 of the array.
* **(`np.reshape`):** It reshapes the array into the desired shape of 6 x 6 ndarray.
* **(`np.mean()`):** The mean for the given Boolean Condition of S.
* **(`S[S_mean < S]`):** The Boolean Condition to get the value of the above mean.
* **(`print(len(above_mean))`):** The length of elements stored in above_mean.
* **(`np.save("above_mean.npy", above_mean)`):** It saves a single NumPy array "above_mean" into the computer in a binary file called "above_mean.npy".
```
S = np.arange(1,37,1)

S = S**2

S = np.reshape(S,(6,6))
print(S)

S_mean = np.mean(S)
print(S_mean)

above_mean = S[S_mean < S]
print(above_mean)

print(len(above_mean))

np.save("above_mean.npy", above_mean)
```
# README File Version History
September 3, 2026: Initial README file output uploaded.
