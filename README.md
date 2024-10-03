Tingwei Adeck
October 03, 2024

<!-- README.md is generated from README.Rmd. Please edit that file -->

# screenRes

The goal of screenRes is to get the screen resolution of screens.

## Installation

You can install the development version of screenRes from
[GitHub](https://github.com/) with:

``` r
#install.packages("devtools")
devtools::install_github("AlphaPrime7/screenRes")
```

## Example

This is a basic example of screenRes:

``` r
library(screenRes)
screen_res_dos_unix(screen_number = 3) / 2
#> The screen resolution is 7680x4320 on the  unix platform
#> [1] 3840 2160
screen_res_win()
#> Warning in screen_res_win(): The function is not designed for the unix platform
#> NULL
#The issue with unix is returning summed screen resolutions when multiple screens are involved.
```

Alternative:

``` r
library(rpanel)
#> Loading required package: tcltk
#> Package `rpanel', version 1.1-5: type help(rpanel) for summary information
rpanel::rp.screenresolution()
#> $width
#> [1] 7665
#> 
#> $height
#> [1] 4290
rpanel::rp.screenresolution()$width/2
#> [1] 3832.5

#rJava is good alternative as well-Issues with java config prohibit its demonstration.
```

## Conclusion

A one document package for getting the screen resolution. Seems to
provide better results than `rpanel` but very similar.
