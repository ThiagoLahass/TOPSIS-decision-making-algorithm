# TOPSIS Algorithm

## Summary

The TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) algorithm is a decision-making technique used to determine the best alternative among a set of options based on multiple criteria. It calculates the relative closeness of each alternative to an ideal solution and ranks them accordingly.

## Purpose

The purpose of the TOPSIS algorithm is to assist in decision-making processes where there are multiple criteria to consider. It helps in selecting the most suitable alternative by evaluating their performance against the ideal solution.

## Calculation Method

1. **Normalization**:
   - Normalize the decision matrix to bring all criteria on the same scale. This involves dividing each element of the matrix by the square root of the sum of squares of all elements in the column.

2. **Weighted Normalization**:
   - Apply weights to the normalized matrix based on the importance of each criterion. This is achieved by multiplying each normalized value by the corresponding weight.

3. **Ideal Solution Calculation**:
   - Determine the positive ideal solution (A+) and negative ideal solution (A-) for benefit and cost criteria, respectively. A+ contains the maximum values for each criterion, while A- contains the minimum values.

4. **Distance Calculation**:
   - Calculate the Euclidean distance of each alternative from the ideal solutions. For A+, the distance is calculated as the square root of the sum of squares of differences between each alternative's normalized value and the corresponding value in A+.

5. **Proximity Measure**:
   - Calculate the relative proximity of each alternative to the ideal solutions. This is done by dividing the distance from A- by the sum of distances from A+ and A-.

6. **Ranking**:
   - Rank the alternatives based on their proximity measure. Higher values indicate better alternatives, as they are closer to the ideal solution.

## Example

Consider a decision matrix D with alternatives A1, A2, A3 and criteria C1, C2, C3, C4:

|       | C1 | C2 | C3  | C4  |
|-------|----|----|-----|-----|
| A1    | 15 | 6  | 25000 | 7  |
| A2    | 12 | 7  | 35000 | 7  |
| A3    | 10 | 9  | 55000 | 8  |

Weights W: [0.3, 0.05, 0.6, 0.05]

1. **Normalize matrix D**:
   - Calculate the normalized decision matrix by dividing each element by the square root of the sum of squares of all elements in the respective column.

2. **Apply weights**:
   - Multiply each normalized value by the corresponding weight to obtain the weighted normalized matrix P.

3. **Calculate ideal solutions**:
   - Determine the positive ideal solution A+ and negative ideal solution A- using max and min operations, respectively.

4. **Calculate distances**:
   - Compute the Euclidean distances of each alternative from A+ and A-.

5. **Compute proximity measures**:
   - Calculate the relative proximity of each alternative by dividing the distance from A- by the sum of distances from A+ and A-.

6. **Rank alternatives**:
   - Rank the alternatives based on their proximity measures. Higher values indicate better alternatives.

This README provides a brief overview of the TOPSIS algorithm. For detailed implementation and code examples, refer to the actual algorithm implementation in your preferred programming language.