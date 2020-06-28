# Multivariate Linear Regression From Scratch
## Math Behind
### Multivariate Regression

Let **Y** be the n x p predicton matrix(Dependent Variable matrix), **X** be an n x (q + 1) matrix such that it contains all entries of the first column are 1′s, and other columns are independent variables. Let **B** be an (q + 1) x p matrix of fixed parameters. The model is:
\begin{equation}
Y = X \cdot B
\end{equation}

Estimation of Y:
\begin{equation}
\hat{Y} = X \cdot \hat{B}
\end{equation}

$\hat{Y}$ is the predicted value that all lie on the regression hyper-plane. Then  the residuals Y - $\hat{Y}$ are orthogonal to the columns of **X** and thus
\begin{equation}
X'\cdot (Y - X \cdot \hat{B}) = 0
\\
X'\cdot Y - X' \cdot X \cdot \hat{B} = 0
\\
X' \cdot X \cdot \hat{B} = X'\cdot Y 
\end{equation}
Hence,
\begin{equation}
\hat{B} = (X' \cdot X)^{-1} \cdot X'\cdot Y
\end{equation}

The least squares estimator $\hat{B}$ is the standardized coefficient estimate, which means we need to scale the predictors **X** (make them unit less) to make slope estimates comparable.These dimensionless regression coefficients are usually called standardized regression coefficients 

## Result
Similar Performance and Accuracy as scikit-learn Implementation

## Dataset
Kaggle: https://www.kaggle.com/kumarajarshi/life-expectancy-who

## Cite
* fastai-v0.7
* http://mezeylab.cb.bscb.cornell.edu/labmembers/documents/supplement%205%20-%20multiple%20regression.pdf
* https://brilliant.org/wiki/multivariate-regression/