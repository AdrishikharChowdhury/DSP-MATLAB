# 5. DFT & IDFT

Manual MATLAB implementations of Discrete Fourier Transform (DFT) and Inverse DFT (IDFT) using direct summation formulas.

## Files
- `DFT.txt` / `DFT.mat`  
- `IDFT.txt` / `IDFT.mat`  

## DFT

**Input**
- Time-domain sequence: `xn = [3 -1 0 1]`  
- Length: `N = 4`  

**Formula**

X[k] = Σ[n=0 to N-1] xn[n] ⋅ exp(-j2πkn/N), k=0 to N-1


**Process**
- Double nested loop computes all N frequency bins `X[k]`.  
- Calculates magnitude response: `abs(X)`  
- Calculates phase response: `angle(X)`  

**Output / Plots**
- Stem plots of:
  - Input sequence `xn`  
  - Magnitude spectrum `abs(X)`  
  - Phase spectrum `angle(X)`  

## IDFT

**Input**
- Frequency-domain sequence: `X = [3, 3+2i, 3, 3-2i]`  
- Length: `N = 4`  

**Formula**

x[n] = (1/N) Σ[k=0 to N-1] X[k] ⋅ exp(j2πkn/N), n=0 to N-1


**Process**
- Double nested loop recovers time-domain sequence `x[n]`.  
- Scales by `1/N` factor.  

## How to Run

1. Open MATLAB / GNU Octave in the `5. DFT & IDFT` folder.  
2. Optionally load the data file (e.g., `load('DFT.mat')` or `load('IDFT.mat')`).  
3. Save each `.txt` as a `.m` file with the same base name and run it.  
4. Verify: `ifft(fft(xn))` should match original `xn` within numerical precision.