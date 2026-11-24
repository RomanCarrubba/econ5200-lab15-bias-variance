# econ5200-lab15-bias-variance

# Bias, Variance and an Unbiased Cross-Validation Score

## Objective
I studied how well cross-validation estimates a model's true error, and how that error divides into bias squared, variance and noise.

## Methodology
- I simulated 80 data points and used cross-validation to compare polynomial fits of degree 1 to 12.
- I picked the best degree by cross-validation error.
- I simulated 20,000 new points from the same process and scored the chosen fit on them to get its true error.
- I ran nested cross-validation to get an error estimate that is not affected by the degree selection.
- I split the expected error into bias squared, variance and noise by repeated simulation.
- I wrote my own k-fold cross-validation function for scikit-learn models and checked it against the lab's version using 10 folds and a degree 5 polynomial.

## Key Findings
- I chose degree 5, and its cross-validation error was 0.1853.
- On the 20,000 new points, the true error of that fit was 0.2330.
- Nested cross-validation estimated the error at 0.1910.
- In the error decomposition, noise alone was 0.2025.
- My own k-fold function gave 0.1921 for degree 5 with 10 folds, which I checked against the lab's result.
