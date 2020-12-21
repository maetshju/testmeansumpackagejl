[![Build Status](https://travis-ci.com/maetshju/testmeansumpackagejl.svg?branch=main)](https://travis-ci.com/maetshju/testmeansumpackagejl)

To run the tests as a script, run the command

```bash
julia test/runtests.jl
```

which returns the results
   
            | mean method        | foldl method      
------------|--------------------|-------------------
**array 1** | 249.88746883431702 | 249.88746883431705
**array 2** | 79.97860557454474  | 79.97860557454476

To run the tests using the `Pkg` testing functionality, run the command

```bash
julia -e "using Pkg; Pkg.activate(); Pkg.test()"
```

which gives the results

            | mean method        | foldl method      
------------|--------------------|-------------------
**array 1** | 249.88746883431705 | 249.88746883431705
**array 2** | 79.97860557454476  | 79.97860557454476

The build results can be seen in the Travis CI results, which are accessible with the badge at the top of the README.