# TOPSIS - A Decision Making Algorithm

**Estimated Reading Time: 9 minutes**

## Table of Contents

1. [Introduction](#introduction)
2. [Multi-Criteria Decision Making](#multi-criteria-decision-making)
3. [The TOPSIS Algorithm](#the-topsis-algorithm)
   - [Step 1](#step-1)
   - [Step 2](#step-2)
   - [Step 3](#step-3)
   - [Step 4](#step-4)
4. [Example Code](#example-code)
5. [References](#references)

---

## Introduction

Throughout our lives, we are faced with a series of decisions, some easy and others extremely difficult. Whether easy or hard, making a choice typically involves alternatives to be chosen based on a set of predefined criteria. A simple example could be choosing a car to buy. Most people consider price, engine power, manufacturer reputation, comfort, etc. These are our criteria for choosing a car, and based on them, we evaluate our alternatives, which could be an HB20, a Pálio, or a Corola, depending on which criteria are most important to each person. Now imagine a more complex decision to be made, such as where to invest a certain amount of money. Can you imagine an algorithm that can assist you in this decision?

...

---

## The TOPSIS Algorithm

Below are the step-by-step details of the TOPSIS decision-making algorithm.

### Step 1

Identify the positive ideal solution 
A
+
 for benefit criteria and the negative ideal solution 
A
−
 for cost criteria, as described below:

\[ A+ = (p+1, p+2, \cdots, p+n) \]
\[ A- = (p-1, p-2, \cdots, p-n) \]

Where:

\[ p+_{j} = \begin{cases} \max_{i}(p_{ij}), & \text{if the criterion is benefit} \\ \min_{i}(p_{ij}), & \text{if the criterion is cost} \end{cases} \]

\[ p-_{j} = \begin{cases} \min_{i}(p_{ij}), & \text{if the criterion is benefit} \\ \max_{i}(p_{ij}), & \text{if the criterion is cost} \end{cases} \]

...

---

## Example Code

```python
import numpy as np

def normalize_matrix(matrix):
    return matrix / np.sqrt(np.sum(matrix**2, axis=0))

def weighted_normalized_matrix(matrix, weights):
    return matrix * weights

# Example usage
D = np.array([[15, 6, 25000, 7], [12, 7, 35000, 7], [10, 9, 55000, 8]])
W = np.array([0.3, 0.05, 0.6, 0.05])

# Normalize the matrix
R = normalize_matrix(D)

# Apply weights
P = weighted_normalized_matrix(R, W)

# Perform TOPSIS calculations...

