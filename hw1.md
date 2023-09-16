P8104 HW 1 LEL2176
================

# Problem 1

``` r
#load in library and dataset
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.3     ✔ readr     2.1.4
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.0
    ## ✔ ggplot2   3.4.3     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.2     ✔ tidyr     1.3.0
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
library(moderndive)
data("early_january_weather")
```

``` r
weather_scat = ggplot(early_january_weather, aes(x = time_hour, y  = temp, color = "humid")) + geom_point()
weather_scat
```

![](hw1_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

``` r
ggsave("weather_scat.pdf")
```

    ## Saving 7 x 5 in image

# Problem 2

``` r
plot_df = 
  tibble(
    x = rnorm(10),
    vec_logical = c(x>0),
    vec_char = c("Child", "Adult", "Old Age", "Old Age", "Adult", "Old Age",
                 "Child", "Adult", "Adult", "Child"),
    vec_fact = factor(vec_char, levels = c("Child", "Adult", "Old Age"))
  )
```
