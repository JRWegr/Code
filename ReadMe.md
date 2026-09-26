# ADEC7430.01 Fall 2026 ML/AI Algorithms I Coursework

Assignments for ADEC7430.01 Fall 2026 ML/AI Algorithms I at Boston College, Fall 2026.

## Assignments

### HW1: Prediction vs. Inference
Simulated house prices with a curved age effect and compared OLS and KNN, both written in numpy. KNN predicted much better (test RMSE 8.18 vs. 16.99), but OLS estimated the square footage effect more accurately. The best model depends on whether the goal is prediction or inference.

Notebook: [WegrzynekHW1.ipynb](WegrzynekHW1.ipynb)

### HW2: Sampling Variability
Generated 50 datasets from the same process using make_regression() and fit a linear regression to each. The real features were estimated consistently, but the noise features ranged from about -4 to 5 and sometimes flipped sign. Test MSE ranged from about 255 to 700. Sampling randomness alone can make irrelevant features look meaningful.

Notebook: [WegrzynekHW2.ipynb](WegrzynekHW2.ipynb)
