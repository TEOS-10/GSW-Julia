[![Build status Linux and macOS](https://travis-ci.org/TEOS-10/GibbsSeaWater.jl.svg?branch=master)](https://travis-ci.org/TEOS-10/GibbsSeaWater.jl)
[![Build status Windows](https://ci.appveyor.com/api/projects/status/77kj4lug424x20y9/branch/master?svg=true)](https://ci.appveyor.com/project/Alexander-Barth/gibbsseawater-jl-ojx2d/branch/master)
[![Coverage Status](https://coveralls.io/repos/TEOS-10/GibbsSeaWater.jl/badge.svg?branch=master&service=github)](https://coveralls.io/github/TEOS-10/GibbsSeaWater.jl?branch=master)


# GibbsSeaWater.jl

GibbsSeaWater.jl is a Julia wrapper for [GSW-C#master](https://github.com/TEOS-10/GSW-C/), which is the C implementation of the Thermodynamic Equation of Seawater 2010 (TEOS-10).

## Installation

Start Julia and issue the following commands:

```julia
using Pkg
Pkg.add(PackageSpec(url="https://github.com/TEOS-10/GibbsSeaWater.jl"))
```

## Example

One should the [vectorized "dot" operator](https://docs.julialang.org/en/v1/manual/mathematical-operations/#man-dot-operators-1) for arrays:

```julia
C = [45.8;34.7]
T = [28.9;22.8]
P = [10.0;50.0]
SP = gsw_sp_from_c.(C,T,P)
```

## About TEOS-10

Please check the [official site](http://www.teos-10.org) and [official repository](https://github.com/TEOS-10), which provide the official implementations (C/Fortran/Matlab/PHP) and the wrappers.
