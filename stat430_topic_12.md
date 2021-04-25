# Bivariate Analysis Correlation

## 1. Pearson Correlation
### Plot points:
```
PROC PLOT DATA=SET1;
PLOT AGE*WEIGHT=GENDER;
RUN;
```
### Show Correlation between three variables
```
proc corr data=set1;
title 'some title';
var hight weight age;
run;
```
### Shoe correlation between two variables
```
proc corr data=set1 pearson nosimple;
var hight weight;
with age;
run;
```

## 2. Spearman Correlation
Notes:
- Use the option NOSIMPLE if simple statistics are not needed
- To get SPEARMAN CORR(Non-parametric correlation coefficients based on ranksrather than data values), we must use the PEARSON option as well.

```
PROC CORR DATA=SET1 PEARSON SPEARMAN NOSIMPLE;
TITLE ’EXAMPLE OF CORR MATRIX’;
VAR HEIGHT WEIGHT AGE;
RUN;
```

## 3. Partial Correlation
Notes:
- Remove the effect of third variable
```
PROC CORR DATA=SET1 PEARSON NOSIMPLE;
VAR HEIGHT WEIGHT;
PARTIAL AGE;
RUN;
```
