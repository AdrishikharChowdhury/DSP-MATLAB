
# 2. Linear Convolution

This folder contains MATLAB scripts and corresponding `.mat` data files for implementing and visualizing linear convolution and related operations such as convolution properties, auto-correlation, and cross-correlation. 

## File Structure

- `Convolution-of-2-signals.txt`  
- `Convolution-of-2-signals.mat`  
- `Convolution-Property.txt`  
- `Convolution-Property.mat`  
- `Auto-Correlation.txt`  
- `Auto-Correlation.mat`  
- `Cross-Correlation.txt`  
- `Cross-Correlation.mat`  

Each `.txt` file contains MATLAB code that can be used as a script, and each `.mat` file is assumed to store related signal data or parameters for the corresponding experiment.

## Scripts Overview

### `Convolution-of-2-signals`

- Defines two finite-length sequences `x1` and `x2` and plots them using `stem`.
- Illustrates the step-by-step convolution process by time-reversing and shifting one sequence (`x2(-n)`, `x2(k-n)`) in multiple subplots, and finally plots the convoluted output `conv(x1,x2)`.

### `Convolution-Property`

- Uses three sequences `x1`, `x2`, and `x3` to demonstrate convolution properties.
- Verifies:
  - Commutative property: `conv(x1,x2)` vs `conv(x2,x1)`  
  - Associative property: `conv(x1,conv(x2,x3))` vs `conv(conv(x1,x2),x3)`  
  - Distributive property: `conv(x1,x2+x3)` vs `conv(x1,x2)+conv(x1,x3)`  
  All results are visualized in a 3×3 grid of `stem` plots with proper axis labels.

### `Auto-Correlation`

- Defines a single input sequence `x1` and computes its auto-correlation using `autocorr(x1)`.
- Plots the original signal and the auto-correlated output side-by-side using `stem`, with time and amplitude labels.

### `Cross-Correlation`

- Defines two sequences `x1` and `x2` and computes their cross-correlation using `xcorr(x1,x2)`.
- Displays the first signal, second signal, and cross-correlated output in three subplots, all with time and amplitude axes labeled.
## How to Use

1. Open MATLAB or GNU Octave in the `2. Linear Convolution` folder.
2. Optionally load the `.mat` file for the experiment you want:
   - `load('Convolution-of-2-signals.mat')`, `load('Convolution-Property.mat')`, `load('Auto-Correlation.mat')`, or `load('Cross-Correlation.mat')`.
3. Copy the corresponding `.txt` code into a `.m` script with the same base name and run it.
4. Observe the figures to understand linear convolution, its properties, and the relationships between auto-correlation and cross-correlation.