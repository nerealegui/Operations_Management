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



```mermaid
flowchart TD
    A[Is the Data Stationary?]
    B[Is the Data Uncorrelated?]
    C[Is the Data Normally Distributed?]
    D[Is the Data White Noise?]
    E[Do We Need a Linear Model?]
    F[Is the Data Gaussian White Noise?]
    G[Is the Data Strict White Noise?]
    H[Is the Data Independent?]
    I[Do We Need a Non-Linear Model?]
    J[Do We Need Transformations?]

    A -->|p-value of ADF test <= 0.05| B
    B -->|lb_pvalue of Box test > 0.05| C
    C -->|p-value of Shapiro-Wilk test > 0.05| D
    D -->|mean ≈ 0, variance > 0, lb_pvalue of Box test > 0.05| E
    E -->|p-value of ADF test <= 0.05, lb_pvalue of Box test <= 0.05| F
    F -->|p-value of Shapiro-Wilk test > 0.05, mean ≈ 0, variance > 0, lb_pvalue of Box test > 0.05| G
    G -->|mean ≈ 0, variance > 0, lb_pvalue of Box test > 0.05| H
    H -->|p-value of Shapiro-Wilk test > 0.05, lb_pvalue of Box test > 0.05| I
    I -->|lb_pvalue of Ljung-Box test on squared residuals <= 0.05| J
    J -->|p-value of ADF test > 0.05| A