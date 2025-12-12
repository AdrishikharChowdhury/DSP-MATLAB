<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 7. Z Transform

MATLAB Symbolic Math Toolbox demonstrations of Z-transform properties, forward/inverse transforms, and partial fraction inverse Z-transform.

## Files

- `Properties.txt` / `Properties.mat`
- `Z-transform-Inverse.txt` / `Z-transform-Inverse.mat`
- `inverse-Z-using-Partial-Fraction.txt` / `inverse-Z-using-Partial-Fraction.mat`


## Properties

**Input**

- Linear combination: `x_n = 2*(1/2)^n + 3*(1/4)^n`, `u(n)`
- Time shift: `(1/3)^n` shifted by `k=2`
- Convolution: `x=[1 2 3 4]`, `h=[1 1 1 1]`

**Properties Verified**

- Linearity: `Z{a*x1 + b*x2} = a*Z{x1} + b*Z{x2}`
- Time shift: `Z{x(n-k)} = z^{-k}X(z)`
- Convolution: `Z{x(n)*h(n)} = X(z)H(z)`

**Output**: Symbolic pretty-print of LHS vs RHS for each property.

## Z-transform-Inverse

**Input**

- `x1_n = (1/4)^n`
- `x2_n = sin(w0*n)`
- `x3_n = cos(w0*n)`

**Process**

```
X_z = ztrans(x_n, n, z)
x_n = iztrans(X_z, n, z)
```

**Output**: Pretty-print pairs showing forward Z → inverse Z recovery for exponential, sine, cosine signals.

## inverse-Z-using-Partial-Fraction

**Input**

```
H(z) = (z+5)/(z^2 + 3z + 2)
```

**Process**

```
Y(z) = H(z)/z
Y_partial = partfrac(Y(z))
h[n] = iztrans(z * Y_partial)
```

**Output**: Partial fraction expansion of `H(z)` and time-domain `h[n]`.

## How to Run

1. Open MATLAB with Symbolic Math Toolbox in the `7. Z Transform` folder.
2. Optionally load the data file (e.g., `load('Properties.mat')`).
3. Save each `.txt` as a `.m` file with the same base name and run it.
4. Check console for symbolic pretty-printed expressions verifying Z-transform properties.
<span style="display:none">[^1][^2][^3]</span>

<div align="center">⁂</div>

[^1]: Properties.txt

[^2]: Z-transform-Inverse.txt

[^3]: inverse-Z-using-Partial-Fraction.txt

