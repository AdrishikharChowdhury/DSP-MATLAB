<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 8. IIR \& FIR

MATLAB implementations of FIR filter design using windowing methods and IIR Butterworth low-pass/high-pass filters with magnitude/phase responses.

## Files

- `Reactangular-and-Hamming-Window.txt` / `Reactangular-and-Hamming-Window.mat`
- `Rectangular-and-Blackman-Window.txt` / `Rectangular-and-Blackman-Window.mat`
- `Butterworth-Filter-LPF.txt` / `Butterworth-Filter-LPF.mat`
- `Butterworth-Filter-HPF.txt` / `Butterworth-Filter-HPF.mat`


## FIR Window Design (Low-pass)

**Common Parameters**

- Filter length: `N = 25`
- Cutoff: `wc = 0.5π`
- Ideal low-pass impulse response: `hd[n]` using sinc function


### Rectangular + Hamming

**Windows**: `boxcar(N)` vs `hamming(N)`
**Plots**: Magnitude response `freqz(hn,1,w)` for normalized frequency 0 to π[^1]

### Rectangular + Blackman

**Windows**: `boxcar(N)` vs `blackman(N)`
**Plots**: Magnitude response showing sidelobe reduction with Blackman window[^2]

## IIR Butterworth Filters

**Specifications**

- Passband ripple: `alphap = 4 dB`
- Stopband attenuation: `alphas = 30 dB`
- Passband freq: `fp = 800 Hz`
- Stopband freq: `fs = 400 Hz`
- Sampling freq: `F = 2000 Hz`


### Butterworth LPF

```
[n,wn] = buttord(omp,oms,alphap,alphas)
[b,a] = butter(n,wn)
```

**Plots**: Gain (dB) and phase response over full frequency range[^3]

### Butterworth HPF

```
[b,a] = butter(n,wn,'high')
```

**Plots**: Gain (dB) and phase response[^4]

## How to Run

1. Open MATLAB / GNU Octave in the `8. IIR & FIR` folder.
2. Optionally load the data file for each script.
3. Save each `.txt` as a `.m` file with the same base name and run it.
4. Compare window effects on sidelobes and Butterworth filter characteristics.

<div align="center">⁂</div>

[^1]: Reactangular-and-Hamming-Window.txt

[^2]: Rectangular-and-Blackman-Window.txt

[^3]: Butterworth-Filter-LPF.txt

[^4]: Butterworth-Filter-HPF.txt

