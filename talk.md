class: center, middle

<img src="img/logo.png" style="height: 200px;"/>

# Numgrid and other developments

## Radovan Bast [@\_\_radovan](https://twitter.com/__radovan)

## Text is CC-BY

---

<img src="img/potatos.jpg" style="width: 100%;"/>

.cite[https://www.reddit.com/r/mathmemes/comments/imy8jj/id_make_the_reverse_of_this_joke_but_it_would_be/]

---

# Plan

.left-column60[
### - How molecular integration grids work
### - Numgrid: https://github.com/dftlibs/numgrid
### - Demonstration
### - Why Rust?
### - Ongoing work/ future plans
]
.right-column40[
<img src="img/avatar.jpeg" style="width: 50%;"/>
]

---

class: center, middle, inverse

# Why Rust?

---

## Why [Rust](https://www.rust-lang.org/)?

- .emph[Fast but also safe]
- Memory safety
- Thread safety
- Type system and type safety
- Zero cost abstractions
- Compiler catches most errors (if it compiles, it often just works)
- Compiler provides helpful error messages
- Private and immutable by default
- Great tooling (testing, documentation, auto-formatter, dependency management, package registry, no makefiles needed)
- Community
- Most-loved programming language in the 2016, 2017, 2018, 2019, and 2020
  [Stack Overflow annual surveys](https://insights.stackoverflow.com/survey/)


### More reading

- More info and resources: https://github.com/dev-cafe/rust-demo
- [J. M. Perkel, "Why scientists are turning to Rust", Nature 588, 185-186 (2020)](https://doi.org/10.1038/d41586-020-03382-2)

---

## Why [Rust](https://www.rust-lang.org/)?

.quote["But is it as fast as Fortran/C/C++?"]
- Yes!

.quote["How about math/scientific libraries?"]
- It has very good inter-op with C (and Python) so you can link to any C interface.

.quote["How about shared-memory parallelization?"]
- Very easy to do. And thread safe.

.quote["How about MPI?"]
- A bit early for this. I would do the MPI layer with Python/C/C++/Fortran and
  the intra-node with Rust.

---

class: center, middle, inverse

# The future

---

## Ongoing work (1/2)

### Numerical integration (Python+Rust)

- Future: simpler API, geometric weight derivatives (using automatic differentiation)
  - [Support for more quadratures](https://github.com/dftlibs/numgrid/issues/43)
  - Simpler API
  - Geometric weight derivatives (using automatic differentiation)


### Density evaluation (Python+Rust)

- Goal: Python package for fast densities and density derivatives
- Status: Working on derivatives, to be released in 2021


### Exchange-correlation integration (Python+Rust)

- Goal: Fast and robust code which can serve as reference implementation
- Status: Waiting for the density code to get ready, then relatively trivial

---

## Ongoing work (2/2)

### Exchange-correlation derivatives (Python)

- Arbitrary order exchange-correlation functional derivatives using [JAX](https://jax.readthedocs.io)
- https://github.com/dftlibs/xcauto


### Grimme D3-dispersion energy and their derivatives (Python)

- Collaboration with R. Di Remigio, M. Ringholm, R. Gonzalez
- Status: Writing paper


### Density visualization

- This is what I really want to get to. Super fast and easy to use.
