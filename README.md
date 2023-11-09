
<!-- README.md is generated from README.Rmd. Please edit that file -->

# CountMissingByGroup

<!-- badges: start -->
<!-- badges: end -->

Given a data frame `data` and a column `group`,
`count_all_missing_by_group()` creates a new data frame with one row per
level of `group`. The first column of the output data frame contains the
levels of `group`, and the rest of the columns contain the number of
missing values for all columns in `data` except `group`.

## Installation

You can install the development version of CountMissingByGroup from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("stat545ubc-2023/CountMissingByGroup", ref='0.1.0')
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(CountMissingByGroup)
count_all_missing_by_group(airquality, Month, .groups = "keep")
#> # A tibble: 5 × 6
#> # Groups:   Month [5]
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
```
