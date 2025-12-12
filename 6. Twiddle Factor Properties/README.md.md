<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 6. Twiddle Factor Properties

MATLAB demonstration of twiddle factor properties (periodicity, symmetry) and 8-point twiddle factor computation for FFT.

## Files

- `Periodicity-Symmetry-Properties.txt` / `Periodicity-Symmetry-Properties.mat`
- `8-point-Twiddle-Factor.txt` / `8-point-Twiddle-Factor.mat`


## Periodicity-Symmetry-Properties

**Input**

- Twiddle base: `W = exp(-j2π/N)`, `N = 8`
- Index: `k = 1`, `n = 0:N-1`

**Periodicity Property**

```
W_N^{k(n+N)} = W_N^{kn}
```

**Verification**: `max(abs(W.^(k*(n+N)) - W.^(k*n))) ≈ 0`

**Symmetry Property**

```
(W_N^{kn})* = W_N^{-kn}
```

**Verification**: `max(abs(conj(W.^(k*n)) - W.^(-k*n))) ≈ 0`

**Output**: Console display of property verification errors and twiddle factor values.

## 8-point-Twiddle-Factor

**Input**

- FFT size: `N = 8`

**Process**

```
W_n[i] = exp(-j2πi/N), i = 0:N-1
Wnmag[i] = abs(W_n[i])
Wnphase[i] = angle(W_n[i])
```

**Output**: Arrays `Wn`, `Wnmag`, `Wnphase` containing 8-point twiddle factors, magnitudes, and phases.

## How to Run

1. Open MATLAB / GNU Octave in the `6. Twiddle Factor Properties` folder.
2. Optionally load the data file (e.g., `load('Periodicity-Symmetry-Properties.mat')`).
3. Save each `.txt` as a `.m` file with the same base name and run it.
4. Check console output for property verification (should show errors ≈ 0).
