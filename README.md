
<!-- README.md is generated from README.Rmd. Please edit that file -->

# agua

<!-- badges: start -->
<!-- badges: end -->

agua enables users to fit, optimize, and evaluate models via
[h2o](https://h2o.ai) using a tidymodels interface.

Most users will not have to use aqua directly; the features can be
accessed via a parsnip engine value of `'h2o'`.

There are two main components in agua:

-   parsnip engine definitions for the following models:
-   Infrastructure for the tune and finetune packages.

When fitting a parsnip model, the data are passed to the h2o server
directly. For tuning, the data are passed once and instructions are
given to `h2o.grid()` to process them.

This work is based on @stevenpawley’s
[h2oparsnip](https://github.com/stevenpawley/h2oparsnip) package and
additional work by Qiushi Yan on his summer internship at RStudio.

## Installation

You can install the development version of agua like so:

``` r
require(pak)
pak::pak(c("topepo/agua"))
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(tidymodels)
library(agua)

tidymodels_prefer()

# Start the h2o server before running models
h2o::h2o.init()
```

## Code of Conduct

Please note that the agua project is released with a [Contributor Code
of
Conduct](https://contributor-covenant.org/version/2/0/CODE_OF_CONDUCT.html).
By contributing to this project, you agree to abide by its terms.
