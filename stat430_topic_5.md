# Topic 5 data and data display
## Pie chart
```
proc gchart data=dataline;
title "some_title"
format sales dollar8.;
pie var / sumvar = var2;
run;
```
note
- pie var: specifies what values to show
- sumvar: specifies a numeric variable for sum or mean calculations
## Bar graph
```
proc gchart data=some_data;
vbar var / type = percent;
title "some title";
run;
```
## Histogram
```
proc univariate data=somedata noprint;
histogram some_var / endpoints = 3.425 to 3.6 by .025;
run;
```
## Boxplots
```
proc univariate data = some_data plot;
var var_name
run;
```