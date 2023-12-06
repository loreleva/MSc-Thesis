# MSc-Thesis
My thesis for the MSc degree in Computer Science.

The work presents a **new method** to statistically find the global optimum of a Black-Box function.
This new statistical method takes in input two real values $\delta, \epsilon \in \left(0,1\right)$, a Black-Box optimizer $BBO$ and a Black-Box function $f$, and returns in output a solution $S$ such that, with statistical confidence $1 - \delta$,
the probability that $BBO$ returns a solution better than $S$ on $f$ is $< \epsilon$.

This new method has been tested with the ``NGOpt`` optimizer of [Nevergrad](https://facebookresearch.github.io/nevergrad/index.html) 
and with the [``NOMAD``](https://nomad-4-user-guide.readthedocs.io/en/latest/) optimizer, which implements the [MADS](https://dl.acm.org/doi/abs/10.1145/1916461.1916468) algorithm.

A comparison with DIRECT, a state-of-the-art algorithm in Black-Box Global Optimization, has been made, more precisely with its variant [``DIRECT-GL``](https://link.springer.com/article/10.1007/s11590-017-1228-4).

The results of the tests on the [optimization test functions](https://www.sfu.ca/~ssurjano/optimization.html) showed that the new statistical method applied to ``NGOpt`` and ``NOMAD`` found the global optimum on all the test functions,
while ``DIRECT-GL`` didn't solve a large portion of high-dimensional problems.
