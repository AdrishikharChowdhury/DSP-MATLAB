# 3. Circular Convolution

This folder contains a MATLAB script and corresponding `.mat` data file for performing circular convolution, applying zero-padding, and comparing circular convolution with linear convolution. [file:8]

## File Structure

- `Circular-Convolution-and-comparison.txt`  
- `Circular-Convolution-and-comparison.mat`  

The `.txt` file contains MATLAB code suitable for use as a script, and the `.mat` file is assumed to store related sequences or parameters for this experiment.

## Script Overview

### `Circular-Convolution-and-comparison`

- Defines two finite-length sequences `x1` and `x2`, then creates zero-padded versions `x1Pad` and `x2Pad` to a specified common length. [file:8]
- Plots:
  - Original signals `x1` and `x2`. [file:8]
  - Circular convolution `cconv(x1,x2)`. [file:8]
  - Zero-padded signals `x1Pad` and `x2Pad`. [file:8]
  - Zero-padded circular convolution `cconv(x1Pad,x2Pad)`. [file:8]
  - Zero-padded linear convolution `conv(x1Pad,x2Pad)`. [file:8]

All results are visualized using `stem` in a 3×3 grid of subplots, with time and amplitude axes labeled for each plot. [file:8]

## How to Use

1. Open MATLAB or GNU Octave in the `3. Circular Convolution` folder.
2. Optionally load the `.mat` file:
   - `load('Circular-Convolution-and-comparison.mat')`. [file:8]
3. Copy the code from `Circular-Convolution-and-comparison.txt` into `Circular-Convolution-and-comparison.m` and run the script.
4. Inspect the figures to understand circular convolution, the effect of zero-padding, and how circular and linear convolution outputs differ.