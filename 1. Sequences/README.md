# 1. Sequences

This folder contains MATLAB scripts and corresponding `.mat` data files for basic discrete-time signal and sequence operations, intended for introductory DSP/Signals lab work. [file:1][file:2][file:3]

## File Structure

- `Signal-Mathematics.txt`  
- `Signal-Mathematics.mat`  
- `Time-Operations.txt`  
- `Time-Operations.mat`  
- `Types-of-Sequences.txt`  
- `Types-of-Sequences.mat`  

Each `.txt` file contains MATLAB code that can be copied into a `.m` script or run section-wise in MATLAB/Octave, and each `.mat` file is assumed to store data related to that script (such as generated sequences or parameters). [file:1][file:2][file:3]

## Scripts Overview

### `Types-of-Sequences`

Demonstrates basic sequence types:
- Unit step sequence using a constant-valued vector. [file:2]
- Sinusoidal sequence using \( \sin(y) \). [file:2]
- Exponential sequence using \( \exp(y) \). [file:2]

The script uses `stem` plots in a 2×2 subplot layout and labels time on the x-axis and amplitude on the y-axis. [file:2]

### `Signal-Mathematics`

Illustrates arithmetic operations on two sinusoidal signals:
- Defines two time ranges \( x \) and \( y \) and plots their corresponding sine signals. [file:3]
- Performs addition, subtraction, and pointwise multiplication of the two signals. [file:3]

Results are shown using `stem` in a 2×3 subplot figure with appropriate titles and axis labels. [file:3]

### `Time-Operations`

Focuses on basic time-domain operations on a sinusoidal sequence:
- Original sequence \( \sin(a) \). [file:1]
- Delayed sequence \( \sin(a - 5) \). [file:1]
- Advanced sequence \( \sin(a + 5) \). [file:1]
- Scaled sequence \( \sin(5a) \). [file:1]
- Time-reversed sequence \( \sin(-a) \). [file:1]

These are visualized in a 2×3 subplot figure with consistent axis labels (Time / Amplitude). [file:1]

## How to Use

1. Open MATLAB or GNU Octave.
2. Load the corresponding `.mat` file if you want pre-saved variables:
   - `load('Types-of-Sequences.mat')`, `load('Signal-Mathematics.mat')`, or `load('Time-Operations.mat')`.
3. Copy the code from the `.txt` file into a new script with the same base name (for example, `Signal-Mathematics.m`) and run it.
4. Inspect the figures to understand the behavior of each sequence and operation. 
