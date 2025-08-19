# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
Date:
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
```
NAME: JAGANNIVASH U M
REG NO: 212224240059
```
```py
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Generate synthetic time series data with trend + noise
np.random.seed(42)
time = np.arange(1, 51)
data = 2*time + np.random.normal(0, 5, 50)   # linear trend with noise

# Original Data Plot
plt.figure(figsize=(10,4))
plt.scatter(time, data, label="Original Data", color="blue")
plt.title("Time Series Data with Trend")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()

# ============================
# A - LINEAR TREND ESTIMATION
# ============================
coeffs_linear = np.polyfit(time, data, 1)  # degree 1 (linear)
linear_trend = np.polyval(coeffs_linear, time)

print("\nA - LINEAR TREND ESTIMATION")
plt.figure(figsize=(10,4))
plt.scatter(time, data, color="blue", label="Original Data")
plt.plot(time, linear_trend, color="red", linewidth=2, label="Linear Trend")
plt.title("Linear Trend Estimation")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()

# =================================
# B - POLYNOMIAL TREND ESTIMATION
# =================================
coeffs_poly = np.polyfit(time, data, 2)  # degree 2 (quadratic)
poly_trend = np.polyval(coeffs_poly, time)

print("\nB - POLYNOMIAL TREND ESTIMATION")
plt.figure(figsize=(10,4))
plt.scatter(time, data, color="blue", label="Original Data")
plt.plot(time, poly_trend, color="green", linewidth=2, label="Polynomial Trend (Quadratic)")
plt.title("Polynomial Trend Estimation")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()
``` 
### OUTPUT
### ORIGINAL DATA:
<img width="1165" height="492" alt="Screenshot 2025-08-19 135153" src="https://github.com/user-attachments/assets/34302a3f-a5b0-484e-96a0-8323de94f72d" />


### A - LINEAR TREND ESTIMATION:
<img width="1173" height="565" alt="Screenshot 2025-08-19 135318" src="https://github.com/user-attachments/assets/30b0bba6-18fa-4294-8af6-05240bc16249" />


### B- POLYNOMIAL TREND ESTIMATION:
<img width="1183" height="571" alt="Screenshot 2025-08-19 135341" src="https://github.com/user-attachments/assets/52b5707b-f8e5-446f-a43e-8ba49163fbf2" />


### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
