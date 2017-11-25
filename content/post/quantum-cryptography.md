+++
date = 2016-04-20
lastmod = 2017-09-03
draft = false
tags = ["edx", "caltech"]
title = "Quantum Cryptography"
math = true
summary = """
This interdisciplinary course is an introduction to the exciting field of quantum cryptography, developed in collaboration between QuTech at Delft University of Technology and the California Institute of Technology.
"""

[header]
image = "headers/quantum-cryptography.jpg"
+++

{{% toc %}}

# Week 0

The first week is an optional introduction to quantum information. I elected to
carefully work through the materials to get oriented.

- Lecture videos
- Lecture notes
- Julia notebooks

The fourth exercise required me to compute the probabilities of obtaining
measurement outcomes 0 and 1 for three different states.

The measurement basis 

$$\\{ \left| b\_0 \right\rangle , \left| b\_1 \right\rangle \\}$$

was as follows

$$
\left| b\_0 \right\rangle = \sqrt{\frac{1}{3}} \left| 0 \right\rangle
+ \sqrt{\frac{2}{3}} \left| 1 \right\rangle, \\\\\\
\left| b\_1 \right\rangle = \sqrt{\frac{2}{3}} \left| 0 \right\rangle
- \sqrt{\frac{1}{3}} \left| 1 \right\rangle
$$

$$
|\psi\_1 \rangle = |0\rangle
|\psi\_2 \rangle = |+\rangle
|\psi\_2 \rangle = |-\rangle
$$

```julia
b0 = [sqrt(1/3); sqrt(2/3)];
b1 = [sqrt(2/3); -sqrt(1/3)];

# State to be measured
psi1 = [1; 0]
psi2 = [1; 1]/sqrt(2);
psi3 = [1; -1]/sqrt(2);

@test abs(b0' * psi1)[1]^2 ≈ 1/3
```

Output:

    Test Passed
      Expression: (abs(b0' * psi1))[1] ^ 2 ≈ 1 / 3
       Evaluated: 0.3333333333333333 isapprox 0.3333333333333333

# Week 1
# Week 2

