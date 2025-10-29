# Genetic_Algorithm
This is a Genetic Algorithm model to find the optimal solution (maximize or minimize a function).

![maxresdefault](https://github.com/user-attachments/assets/63af54ab-432a-47da-bdea-27684bcd7f41)

Problem model
GAProblem dataclass encapsulates everything the GA needs to know about an objective:
chromosome_type: "bit" (bitstrings) or "real" (real-valued vectors).
dim: chromosome length / dimensionality.
bounds: (lo, hi) only for real-valued problems.
fitness_fn(x) -> float: must return a value to maximize.

Problem factories:
make_onemax(dim): maximize number of ones in a bitstring.
make_sphere(dim, lo, hi): uses fitness = -||x||² so maximizing fitness ≡ minimizing Sphere.
make_rastrigin(dim, lo, hi): fitness = -Rastrigin(x) so maximizing fitness ≡ minimizing Rastrigin.
