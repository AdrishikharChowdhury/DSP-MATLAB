<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# DSP MATLAB

Complete MATLAB laboratory experiments covering discrete-time signal processing fundamentals from basic sequences through advanced filter design.

## Folder Structure

```
DSP MATLAB/
├── 1. Sequences/
├── 2. Linear Convolution/
├── 3. Circular Convolution/
├── 4. Overlap Add and Save Method/
├── 5. DFT & IDFT/
├── 6. Twiddle Factor Properties/
├── 7. Z Transform/
└── 8. IIR & FIR/
```


## Experiments Overview

| Folder | Topic | Key Concepts |
| :-- | :-- | :-- |
| 1. Sequences | Basic Operations | Unit step, sinusoidal, exponential sequences; time shift, scaling, reversal |
| 2. Linear Convolution | Convolution \& Properties | Direct convolution, commutative/associative/distributive properties, auto/cross-correlation |
| 3. Circular Convolution | FFT Convolution | `cconv()` vs `conv()`, zero-padding effects |
| 4. Overlap Methods | Block Convolution | Overlap-Add (OLA), Overlap-Save (OLS) using FFT for long convolutions |
| 5. DFT \& IDFT | Frequency Domain | Manual DFT/IDFT summation formulas, magnitude/phase spectra |
| 6. Twiddle Factors | FFT Foundations | Periodicity `W_N^{k(n+N)}=W_N^{kn}`, symmetry `(W_N^{kn})^*=W_N^{-kn}`, 8-point computation |
| 7. Z Transform | Transform Domain | Properties (linearity, shift, convolution), inverse Z via `iztrans()`, partial fractions |
| 8. IIR \& FIR | Filter Design | Windowing (Rectangular, Hamming, Blackman), Butterworth LPF/HPF design |

## File Conventions

Each experiment folder contains:

- `*.txt` → MATLAB script code (copy to `*.m` to run)
- `*.mat` → Pre-computed data/parameters (optional: `load('filename.mat')`)


## Prerequisites

- **MATLAB** with Signal Processing Toolbox
- **Symbolic Math Toolbox** (for Z-transform experiments)
- **GNU Octave** (alternative, most scripts compatible)


## Usage Instructions

1. Navigate to `DSP MATLAB/` in MATLAB/Octave
2. Enter target folder: `cd('8. IIR & FIR')`
3. **Optional**: `load('Butterworth-Filter-LPF.mat')`
4. Copy `.txt` → `.m`: `copyfile('Butterworth-Filter-LPF.txt', 'Butterworth-Filter-LPF.m')`
5. Run: `Butterworth-Filter-LPF`
6. Analyze generated figures/console output

## Verification Commands

```matlab
% Convolution: compare with direct conv()
y_ola ≈ conv(x,h)

% Transforms: round-trip consistency
ifft(fft(xn)) ≈ xn
iztrans(ztrans(x_n)) ≈ x_n

% Filters: check passband/stopband specs
20*log10(abs(freqz(b,a,wp))) ≈ -alphap
```


## Learning Path

**Recommended order**: 1→2→3→4→5→6→8→7
**Progression**: Time-domain → Convolution → Frequency-domain → Filter design → Transform methods

Each experiment builds on previous concepts with increasing mathematical complexity and practical DSP relevance.

