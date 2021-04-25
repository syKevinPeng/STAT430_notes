# Chapter 13 Simple Linear Regression
## Regression Concept
- $$y=\beta_0 + \beta_1*x$$
- $$\bar{x} = \frac{\sum x}{n}$$
- $$\bar{y} = \frac{\sum y}{n}$$
- $$S_{xx} = \sum(x-\bar{x})^2 = \sum{x^2} - \frac{(\sum{x})^2}{n}$$
- $$S_{yy} = \sum(y-\bar{y})^2 = \sum{y^2} - \frac{(\sum{y})^2}{n}$$
- $$S_{xy} = \sum(x-\bar{x})(y=\bar{y}) = \sum{xy} - \frac{\sum{x}\sum{y}}{n}$$
- $$r = \bar{\rho} = \frac{S_{xy}}{\sqrt{S_{xx}}\sqrt{S_{yy}}}$$
- $$\hat{\beta_1} = \frac{S_{xy}}{S_{xx}}$$
- Error sum of squares (SSE) = $S_{yy} - \hat{\beta_1} S_{xy} = \sum(y_i - \hat{y_i})^2$
- Estimate of $\hat{\sigma}^2 = \frac{SSE}{n-2}$

## Conduct Hypothesis Test
1. When we conduct a hypothesis test for the significance of the lnear regression equation, the hypotheses will be
   - $H_0: \beta_1 = 0$
   - $H_a: \beta_1 \ne 0$
2. PROC REG
```
Proc Reg data = data1;
plots = diagnostic(stats = none); /*output residual plot*/
model Y = X; /*Y = a+b*X*/
run
```
#### Adding a quadratic term
```
# after the input line:
X2 = X**2
/* datalines */
Proc Reg data = data1;/*Y = a+b*X + c*X^2*/
Model Y = X X2; 
run;
```
#### Transform Data
```
Data somedata;
    input x y;
    LogX = LOG(x);
Datalines;
```