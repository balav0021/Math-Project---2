# Kinetic analysis on gaseous and aqueous product formation by mixed anaerobic hydrogen-producing cultures

### APA Citation:
Fang, F., Mu, Y., Sheng, G. P., Yu, H. Q., Li, Y. Y., Kubota, K., & Harada, H. (2013). Kinetic analysis on gaseous and aqueous product formation by mixed anaerobic hydrogen-producing cultures. International journal of hydrogen energy, 38(35), 15590-15597.
https://doi.org/10.1016/j.ijhydene.2013.03.157

## Overview
The paper presents a comprehensive investigation into anaerobic hydrogen production by mixed cultures, aiming to understand the kinetics of this process. It introduces an innovative method that combines weighted nonlinear least-squares analysis and an accelerating genetic algorithm to estimate crucial kinetic parameters involved in hydrogen production from sucrose. Through this approach, the study determines key parameters such as maximum substrate uptake rate, substrate uptake affinity constant, and yield coefficient. Validating these estimations with experimental data and comparing them with existing literature, the paper offers a promising and efficient means to analyze and optimize the kinetics of anaerobic hydrogen production, crucial for advancing clean energy generation methods.

<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/ODE.png" width="350"><br>
</p>

## Fitting the Model to Experimental Data
The process entails formulating a set of differential equations modeling anaerobic hydrogen production kinetics, solving them numerically with odeint, and iteratively adjusting parameters like km, ks, Y, and FH2 within the equations to optimize the model's predictive accuracy by comparing simulated substrate concentrations with experimental data.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/S_fit.png" width="350"><br>
</p>

<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/P_fit.png" width="350"><br>
</p>

## Optimizing the Model to Experimental Data
The optimization technique used, curve_fit from SciPy, iteratively refines parameters by minimizing the discrepancy between experimental and simulated data through the fit_function employing the ode_model, achieving the best parameter estimates.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/S_optimized.png" width="350"><br>
</p>

<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/P_optimized.png" width="350"><br>
</p>


## Bifurcation with Parameter ks
The code conducts a bifurcation analysis by systematically altering the parameter ks, plotting the resultant steady-state values of S across the varying ks values, elucidating the impact of ks on the system's behavior and the steady-state concentration of S.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Bifuration_ks.png" width="350"><br>
</p>

## Bifurcation with Parameter Y
The code conducts a bifurcation analysis by systematically altering the parameter Y, plotting the resultant steady-state values of S across the varying ks values, elucidating the impact of Y on the system's behavior and the steady-state concentration of S.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Bifurcation_Y.png" width="350"><br>
</p>

## Sensitivity Analysis
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Sensitivity.png" width="350"><br>
</p>

### Local Sensitivity Analysis
Local sensitivity analysis involves perturbing individual model parameters around nominal values and observing the resulting impact on the model output to assess their relative influence.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Sensitivity_1.png" width="350"><br>
</p>

### Global Sensitivity Analysis

#### Step 1: Generate Data
Global sensitivity analysis involves randomly sampling parameters within defined ranges, integrating the model for each set using Monte Carlo methods, and analyzing resulting outputs to assess the collective influence of parameter variations on model behavior.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Sensitivity_2.png" width="350"><br>
</p>

#### Step 2: Visualize Your Parameter Space
The pairplot function from the seaborn library generates histograms and scatter plots to showcase parameter distributions and relationships, providing an overview of the parameter space for global sensitivity analysis.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Sensitivity_3.png" width="350"><br>
</p>
#### Step 3: Use Least Squares to Estimate the Normalized Sensitivities
The code employs least squares estimation to determine the linear relationship between normalized parameters and the normalized output, facilitating the quantification of parameter sensitivities on the output in a linear regression context.
<p align="center">
  <img src="https://github.com/balav0021/Math-Project---2/blob/main/Sensitivity_4.png" width="350"><br>
</p>




