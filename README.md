## Summary of Results obtained in the analysis of time series

### 1. Is the Data Stationary?
- **Condition:** If the p-value of the ADF test is less than or equal to 0.05.
- **Result:** The process is stationary.

### 2. Is the Data Uncorrelated?
- **Condition:** If the lb_pvalue of the Box test is greater than 0.05.
- **Result:** The residuals are independent.

### 3. Is the Data Normally Distributed?
- **Condition:** If the p-value of the Shapiro-Wilk test is greater than 0.05.
- **Result:** The residuals are normally distributed.

### 4. Is the Data White Noise?
- **Condition:** If the mean is approximately zero, the variance is greater than zero, and the lb_pvalue of the Box test is greater than 0.05.
- **Result:** The data is white noise.

### 5. Is the Data Gaussian White Noise?
- **Condition:** If the p-value of the Shapiro-Wilk test is greater than 0.05, the mean is approximately zero, the variance is greater than zero, and the lb_pvalue of the Box test is greater than 0.05.
- **Result:** The data is Gaussian white noise.

### 6. Is the Data Strict White Noise?
- **Condition:** If the mean is approximately zero, the variance is greater than zero, and the lb_pvalue of the Box test is greater than 0.05.
- **Result:** The data is strict white noise.

### 7. Is the Data Independent?
- **Condition:** If the p-value of the Shapiro-Wilk test is greater than 0.05 and the lb_pvalue of the Box test is greater than 0.05.
- **Result:** The data is independent.

### 8. Do We Need a Linear Model?
- **Condition:** If the p-value of the ADF test is less than or equal to 0.05 and the lb_pvalue of the Box test is less than or equal to 0.05.
- **Result:** The data is stationary and correlated, consider using a linear model.

### 9. Do We Need a Non-Linear Model?
- **Condition:** If the lb_pvalue of the Ljung-Box test on squared residuals is less than or equal to 0.05.
- **Result:** The squared residuals are correlated, consider using a non-linear model.

### 10. Do We Need Transformations?
- **Condition:** If the p-value of the ADF test is greater than 0.05.
- **Result:** The data is not stationary, consider differencing or other transformations.