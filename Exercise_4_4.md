Exercise\_4\_4
================

I need to fix this code block

library(tidyverse)

ggplot(data = mpg) + geom\_point(mapping = aes(x = displ, y = hwy))

fliter(mpg, cyl = 8)

filter(diamond, carat &gt; 3)

``` r
library(tidyverse)
```

    ## -- Attaching packages ----------------------------------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 3.0.0     v purrr   0.2.5
    ## v tibble  1.4.2     v dplyr   0.7.6
    ## v tidyr   0.8.1     v stringr 1.3.1
    ## v readr   1.1.1     v forcats 0.3.0

    ## -- Conflicts -------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = displ, y = hwy))
```

![](Exercise_4_4_files/figure-markdown_github/unnamed-chunk-1-1.png)

``` r
filter(mpg, cyl == 8)
```

    ## # A tibble: 70 x 11
    ##    manufacturer model displ  year   cyl trans drv     cty   hwy fl    cla~
    ##    <chr>        <chr> <dbl> <int> <int> <chr> <chr> <int> <int> <chr> <ch>
    ##  1 audi         a6 q~   4.2  2008     8 auto~ 4        16    23 p     mid~
    ##  2 chevrolet    c150~   5.3  2008     8 auto~ r        14    20 r     suv 
    ##  3 chevrolet    c150~   5.3  2008     8 auto~ r        11    15 e     suv 
    ##  4 chevrolet    c150~   5.3  2008     8 auto~ r        14    20 r     suv 
    ##  5 chevrolet    c150~   5.7  1999     8 auto~ r        13    17 r     suv 
    ##  6 chevrolet    c150~   6    2008     8 auto~ r        12    17 r     suv 
    ##  7 chevrolet    corv~   5.7  1999     8 manu~ r        16    26 p     2se~
    ##  8 chevrolet    corv~   5.7  1999     8 auto~ r        15    23 p     2se~
    ##  9 chevrolet    corv~   6.2  2008     8 manu~ r        16    26 p     2se~
    ## 10 chevrolet    corv~   6.2  2008     8 auto~ r        15    25 p     2se~
    ## # ... with 60 more rows

``` r
filter(diamonds, carat > 3)
```

    ## # A tibble: 32 x 10
    ##    carat cut     color clarity depth table price     x     y     z
    ##    <dbl> <ord>   <ord> <ord>   <dbl> <dbl> <int> <dbl> <dbl> <dbl>
    ##  1  3.01 Premium I     I1       62.7    58  8040  9.1   8.97  5.67
    ##  2  3.11 Fair    J     I1       65.9    57  9823  9.15  9.02  5.98
    ##  3  3.01 Premium F     I1       62.2    56  9925  9.24  9.13  5.73
    ##  4  3.05 Premium E     I1       60.9    58 10453  9.26  9.25  5.66
    ##  5  3.02 Fair    I     I1       65.2    56 10577  9.11  9.02  5.91
    ##  6  3.01 Fair    H     I1       56.1    62 10761  9.54  9.38  5.31
    ##  7  3.65 Fair    H     I1       67.1    53 11668  9.53  9.48  6.38
    ##  8  3.24 Premium H     I1       62.1    58 12300  9.44  9.4   5.85
    ##  9  3.22 Ideal   I     I1       62.6    55 12545  9.49  9.42  5.92
    ## 10  3.5  Ideal   H     I1       62.8    57 12587  9.65  9.59  6.03
    ## # ... with 22 more rows
