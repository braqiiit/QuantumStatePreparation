# Quantum State Preparation

Implementation of the paper [Black-Box Quantum State Preparation without Arithmetic](https://doi.org/10.1103/PhysRevLett.122.020502).

## Problem statement

Given an array of $m$ decimal values 
$$A = (a_0, ..., a_{m-1})$$
such that $a_i \in [0, 1)$, prepare the quantum state 
$$|\psi\rangle = \frac{1}{||A||}\sum_{i=0}^{m-1}a_i|i\rangle$$
where $||A||$ is the normalization constant, and is equal to the magnitude of the vector represented by $A$. $$||A|| = \sqrt{\sum_{i=0}^{m-1}{a_i}^2}$$

We have access to a black-box $amp$ which has the following action - 
$$amp|i\rangle|z\rangle = |i\rangle|z \oplus a_{i}^{(n)}\rangle $$

where $a_{i}^{n}$ is the data $a_{i}$ upto $n$ bits of precision.

## Contents

The Jupyter notebook covers the following - 
1. Grover's standard state preparation method, which requires calculation of arcsines.
2. A modified algorithm which does not require any arithmetic computation, but a comparision operation.
