Pseudo-Dual-Rickart-Code-tester repository

This repository contains codes and tools to analyze and verify whether given examples of semimodules are Pseudo Dual Rickart

The first Python implementation is designed to test the pseudo dual weak Rickart property for semimodules over natural numbers using the GCD operation. The script leverages the combinatorial functionality of the itertools library to analyze all possible functions on the finite set M = {0, 1, ..., n}, where n is a user-defined input.

Functional Highlights:
1. Endomorphism Validation: Functions f: M → M are filtered based on two criteria:
   - f(0) = 0, ensuring that zero maps to zero.
   - Preservation of the GCD operation: f(gcd(x, y)) = gcd(f(x), f(y)), for all x, y ∈ M.

2. Idempotency Check: The function checks if f(f(x)) = f(x), identifying idempotent functions within the set of valid endomorphisms.

3. Extended Image Calculation: The algorithm calculates the extended image of a function f using the logic that a value y ∈ M belongs to the extended image if there exists x1, x2 ∈ M such that max(y, f(x1)) = f(x2).

4. Classification of Semimodules:
   - Pseudo Dual Rickart (Type 2): Determines if every function f has an associated idempotent function g with the same direct image.
   - Pseudo Dual Rickart (Type 1): Examines whether the direct image of f matches its extended image.

5. Performance: The runtime of the program depends exponentially on n, as all possible functions are generated and verified. Computational resources provided by Python's runtime environment are critical.

The second Python implementation replace GCD with MAX operation. One should remarks that Gcd and max play symetric function.
