# formulas by folder (Claude's mapping, standard formulas only)

Every formula here is standard math or science with a folder name attached.
It is a mapping, not a result. M and C in the Atomic Inscribe are the owner's
own definitions, not derived from anything.

## t'pheno (.domain)(div)
```
P = G + E + (G x E) + eps
  [P observed trait, G genotype, E environment, eps noise]
```

## ap'article (articulate / perform at peak)
```
p(a) = p_max * exp( -(a - a*)^2 / (2 * sigma^2) )
a* = argmax_a p(a)
  [inverted-U model of arousal vs performance]
```

## cognee'tz (te'zenzational)
```
P(H | D) = P(D | H) * P(H) / P(D)
```

## data(d'ti)
```
H(X) = - sum_i p(x_i) * log2 p(x_i)
I(X;Y) = H(X) - H(X | Y)
```

## directional'data
```
u = d / ||d||
cos(theta) = (a . b) / (||a|| * ||b||)
```

## e'tensor (sets of reality)
```
T in R^(n1 x n2 x ... x nk)
w_i = sum_j T_ij * v_j
S = {s_1, ..., s_n},  sum_i p_i = 1,  E[f] = sum_i p_i * f(s_i)
  [a set of states with weights, plus contraction]
```

## .weights
```
y_hat = sigma(W x + b)
W <- W - eta * grad_W L
```

## bio'cal (RI'pit)  [register]
```
s_(t+1) = f(s_t, x_t)
cipher.bin = 0   ->   s = 0
```

## spatial'kernel / "makes process re'executable back and forth"
```
run(s0, i) = run(s0, i)        [same input, same output: reproducible]
g(g^-1(x)) = x                 [invertible: back and forth]
f(f(x)) = f(x)                 [idempotent: re-running changes nothing more]
```

## atif' (fieldzs'phzipsz'xompresxcion)  [compaction vs compression]
```
compaction:   f: S -> S',  |S'| = |S|,  f^-1 exists
lossless:     decode(encode(x)) = x
ratio:        R = |raw| / |compressed|
lossy:        d(x, x_hat) <= D,   R(D) = min I(X; X_hat)
K(x) = min { |p| : U(p) = x }
```

## Atomic Inscribe (E, M, C)
```
E := attend(F) -> drop                      [owner's definition]
attention(Q, K, V) = softmax( Q K^T / sqrt(d_k) ) V   [standard formula, closest match to E]
M := matters(brain, what matters)           [owner's definition]
C := consciousness^2                        [owner's definition]
```
