# `gfold`

A C++ implementation of the G-FOLD algorithm.

G-FOLD is an acronym for Guidance for Fuel-Optimal Large
Diverts. It is a guidance algorithm that attempts to find
the best trajectory for powered descent, such as for rocket
boosters and planetary landers. It uses convex optimization
to get as close to the landing target as possible, and then
optimizes for fuel usage to select the most optimal
trajectory.

This project attempts to implement the G-FOLD algorithm in
C++ as a demo that plots the some of the numerical examples
in the original paper using matplotlib-cpp.

# Disclaimer

The algorithm is not fully discretized in this project.

I am also not a rocket scientist. This is a demo - a toy -
not a production-ready piece of code. I make no guarantees
about the correctness nor the functional completeness of
the project. USE AT YOUR OWN RISK!

# Demo

![gfold.png](https://i.postimg.cc/gJDTqd4T/gfold.png)

# Building

#### Prerequisites

  * CMake
  * Eigen
  * Catch2
  * Python3 Matplotlib

#### Build

``` shell
git clone https://github.com/caojohnny/gfold.git
cd gfold
mkdir build && cd build
cmake .. && make
./gfold
```

# Documentation

The G-FOLD algorithm is abstracted to the `gfold.h` and
`gfold.cpp` files. These files are documented, and as such,
it is worth taking a look at their sources and/or
generating HTML documentation for the G-FOLD classes.

A `Doxyfile` has been included with this repository, and
the documentation can be generated by executing the
following command in the root directory using Doxygen:

``` shell
doxygen
```

The generated documentation can be viewed by opening the
`doc/html/index.html` file in your preferred web browser.

# Credits

Built with [CLion](https://www.jetbrains.com/clion/)

Utilizes:

  * [Eigen](https://eigen.tuxfamily.org/)
  * [Epigraph](https://github.com/EmbersArc/Epigraph)
  * [matplotlib-cpp](https://github.com/lava/matplotlib-cpp)

# References

"Lossless Convexification of Non-Convex Control Bound and
Pointing Constraints of the Soft Landing Optimal Control
Problem." B. Acikmese, J. M. Carson III, and L. Blackmore.
IEEE Transactions on Control Systems Technology, Volume 21,
Issue 6 (2013). [Online]. Available: 
http://larsblackmore.com/iee_tcst13.pdf

B. Acikmecse and S. R. Ploen, "Convex programming approach
to powered descent guidance for mars landing,"Amer. Inst.
Astron. Aeron.J. Guid., Control Dyn., vol. 30, no. 5, pp.
1353–1366, 2007.
