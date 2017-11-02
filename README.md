# Computer simulation of Ulf Dieckmann's model of stationary biological community.

### To compile poisson process simulator, download boost from http://www.boost.org/ , unarchive it and add boost folder to compiler's include directories.

#### Algorithm description
Simulations are written using C++11. Data processing is implemented on Python 3.

There are two versions of simulations.

The first one implements the algorithm based on the plane discretization idea. There might be arbitrary number of individuals in every cell of the grid. One step of the algorithm consists of computing birth and death probabilities matrices of individuals. Now birth and death kernels are considered to be Gaussian with zero expectation, arbitrary variance (can be set in the code parameters) and normalizing factor.

The second implementation based on the Poisson process idea. We simulate continiuos process via Poisson process.

### Usage
To run the first implementation for one dimention case run
```
g++ sim_one_dim.cpp -o sim -std=c++11
```
First implementation for two dimentions case currently doesn't work correctly at the moment (sim_two_dim.cpp).

To run the second implementation (one and dimensions cases are in one file) firstly download [Boost](http://www.boost.org), unarchive it and add Boost folder to compiler's include directories. The run
```
g++ sim_poison.cpp -o sim -std=c++11
```

#### Algorithm description
Simulations are written using C++11. Data processing is implemented on Python 3.
The algorithm is based on idea of coordinate discretization. There might be arbitrary number of individuals in every cell of the grid.
One step of the algorithm consists of computing birth probability matrix of new individuals and possible death of each one. Birth and death kernels are considered to be Gaussian.

### Unimplemented
 * Arbitrary birth and death kernels option
 * Multispecies models
 * Small issues (watch code comments)
