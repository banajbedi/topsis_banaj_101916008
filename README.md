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
Fund Name	P1	P2	P3	P4	P5
M1	0.94	0.88	4.5	39	11.33
M2	0.9	0.81	6.7	68.1	19.13
M3	0.84	0.71	6.4	38.6	11.64
M4	0.77	0.59	3.2	32.1	9.17
M5	0.77	0.59	5	59.1	16.37
M6	0.81	0.66	5.5	45.2	13.04
M7	0.86	0.74	6.2	65.1	18.23
M8	0.61	0.37	5.4	68.9	18.82


Weights (`weights`) is not already normalised will be normalised later in the code.

Information of benefit positive(+) or negative(-) impact criteria should be provided in `impacts`.

<br>

## Output file (result.csv)
![image](https://user-images.githubusercontent.com/83486603/155836615-57a01166-6c6f-47f8-b296-d7a0ccc35395.png)

<br>
The output file contains columns of input file along with two additional columns having **Topsis_score** and **Rank**
