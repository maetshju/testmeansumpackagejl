[![Build Status](https://travis-ci.com/maetshju/testmeansumpackagejl.svg?branch=main)](https://travis-ci.com/maetshju/testmeansumpackagejl)

This concern was resolved in [this Issue](https://github.com/JuliaLang/Pkg.jl/issues/2298) for Pkg. It has to do with the default value for the `check-bounds` argument.

Clone this repo with

```bash
git clone https://github.com/maetshju/testmeansumpackagejl.git
```

and then navigate to the new directory. To run the tests as a script, run the command

```bash
julia test/runtests.jl
```

which returns the results
   
—           | mean method        | foldl method      
------------|--------------------|-------------------
**array 1** | 24988.7468834317   | 24988.746883431704
**array 2** | 3998.9302787272372 | 3998.930278727238

To run the tests using the `Pkg` testing functionality, run the command

```bash
julia -e "using Pkg; Pkg.activate(); Pkg.test()"
```

which gives the results

—           | mean method        | foldl method      
------------|--------------------|-------------------
**array 1** | 24988.746883431704 | 24988.746883431704
**array 2** | 3998.930278727238  | 3998.930278727238

Notice that the results of calling the `mean` function from the `Statistics` package are now the same as the results from calculating the mean using a left-to-right sum with `foldl` and then dividing by the length of the array.

The build results can be seen in the Travis CI results, which are accessible with the badge at the top of the README.
