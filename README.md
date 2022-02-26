# TOPSIS

Submitted By: **Banaj Bedi**.

Type: **Package**.

Title: **TOPSIS method for multiple-criteria decision making (MCDM)**.

Version: **1.0.0**.
Date: **2022-02-26**.
Description: **Evaluation of alternatives based on multiple criteria using TOPSIS method.**.

---

## What is TOPSIS?

**T**echnique for **O**rder **P**reference by **S**imilarity to **I**deal **S**olution
(TOPSIS) originated in the 1980s as a multi-criteria decision making method.
TOPSIS chooses the alternative of shortest Euclidean distance from the ideal solution,
and greatest distance from the negative-ideal solution.

<br>

## How to install this package:

```
>> pip install topsis_banaj_101916008
```

### In Command Prompt

```
>> topsis data.csv "1,1,2,1,2" "+,+,-,-,+" result.csv
```

## Input file (data.csv)

The decision matrix should be constructed with each row representing a Model alternative, and each column representing a criterion like Accuracy, R<sup>2</sup>, Root Mean Squared Error, Correlation, and many more.

0.94	0.88	4.5	39	11.33	0.537265357	2
0.9	0.81	6.7	68.1	19.13	0.50956586	5
0.84	0.71	6.4	38.6	11.64	0.358371417	8
0.77	0.59	3.2	32.1	9.17	0.517778957	3
0.77	0.59	5	59.1	16.37	0.542604192	1
0.81	0.66	5.5	45.2	13.04	0.431283618	7
0.86	0.74	6.2	65.1	18.23	0.514845797	4
0.61	0.37	5.4	68.9	18.82	0.500904238	6
![image](https://user-images.githubusercontent.com/83486603/155836591-4d8f3e4d-3d1a-4a51-85ab-aa53ff411a98.png)


Weights (`weights`) is not already normalised will be normalised later in the code.

Information of benefit positive(+) or negative(-) impact criteria should be provided in `impacts`.

<br>

## Output file (result.csv)

| Model | Correlation | R<sup>2</sup> | RMSE | Accuracy | Topsis_score | Rank |
| ----- | ----------- | ------------- | ---- | -------- | ------------ | ---- |
| M1    | 0.79        | 0.62          | 1.25 | 60.89    | 0.7722       | 2    |
| M2    | 0.66        | 0.44          | 2.89 | 63.07    | 0.2255       | 5    |
| M3    | 0.56        | 0.31          | 1.57 | 62.87    | 0.4388       | 4    |
| M4    | 0.82        | 0.67          | 2.68 | 70.19    | 0.5238       | 3    |
| M5    | 0.75        | 0.56          | 1.3  | 80.39    | 0.8113       | 1    |

<br>
The output file contains columns of input file along with two additional columns having **Topsis_score** and **Rank**
