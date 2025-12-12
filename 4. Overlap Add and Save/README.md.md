<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 4. Overlap Add and Save Method

This folder contains MATLAB scripts and corresponding `.mat` data files implementing fast block convolution via Overlap-Add (OLA) and Overlap-Save (OLS) methods using FFT in the frequency domain.[^1][^2]

## File Structure

- `Overlap-Add-Method.txt` / `Overlap-Add-Method.mat`
- `Overlap-Save-Method.txt` / `Overlap-Save-Method.mat`

The `.txt` files hold complete MATLAB scripts; `.mat` files store related signal and filter data.[^2][^1]

## Scripts Overview

### Overlap-Add-Method

Processes input signal `x` with FIR filter `h` in blocks of length `L`:

- Computes FFT-domain convolution per block: `ifft(fft(xblk,N) .* H)`.
- Overlaps and adds valid output segments to form full convolution `y`.[^1]

**Visualization**: Stem plots of input `x`, impulse response `h`, and output `y`.[^1]

### Overlap-Save-Method

Similar block processing but discards corrupted overlap portions:

- Takes `L` new samples per block, computes circular convolution via FFT.
- Saves only the last `L` valid samples from each `N`-point output block.[^2]

**Visualization**: Stem plots of input `x`, impulse response `h`, and output `y`.[^2]

## Usage Instructions

1. Launch MATLAB/Octave in this folder.
2. **Optional**: `load('Overlap-Add-Method.mat')` or `load('Overlap-Save-Method.mat')`.
3. Copy `.txt` content to matching `.m` file → Run script.
4. Verify outputs match direct `conv(x,h)` for correctness.[^1][^2]

<div align="center">⁂</div>

[^1]: Overlap-Add-Method.txt

[^2]: Overlap-Save-Method.txt

