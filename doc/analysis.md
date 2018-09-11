Test RMD
================
Gregory Vitz
2018-09-10

Load the Data!

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
library(here)
```

    ## here() starts at C:/Users/Greg/Documents/projects/cats_vs_dogs

``` r
library(rio)

cnd <- import(here("data", "cats_vs_dogs.csv"))
```

``` r
glimpse(cnd)
```

    ## Observations: 49
    ## Variables: 13
    ## $ V1                     <int> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, ...
    ## $ state                  <chr> "Alabama", "Arizona", "Arkansas", "Cali...
    ## $ n_households           <int> 1828, 2515, 1148, 12974, 1986, 1337, 33...
    ## $ percent_pet_households <dbl> 59.5, 59.5, 62.4, 52.9, 61.3, 54.4, 56....
    ## $ n_pet_households       <int> 1088, 1497, 716, 6865, 1217, 728, 189, ...
    ## $ percent_dog_owners     <dbl> 44.1, 40.1, 47.9, 32.8, 42.5, 28.3, 33....
    ## $ n_dog_households       <int> 807, 1008, 550, 4260, 845, 379, 113, 38...
    ## $ avg_dogs_per_household <dbl> 1.7, 1.8, 2.0, 1.6, 1.6, 1.3, 1.4, 1.1,...
    ## $ dog_population         <int> 1410, 1798, 1097, 6687, 1349, 507, 163,...
    ## $ percent_cat_owners     <dbl> 27.4, 29.6, 30.6, 28.3, 32.3, 31.9, 33....
    ## $ n_cat_households       <int> 501, 743, 351, 3687, 642, 427, 113, 33,...
    ## $ avg_cats_per_household <dbl> 2.5, 1.9, 2.3, 1.9, 1.9, 1.9, 1.7, 1.9,...
    ## $ cat_population         <int> 1252, 1438, 810, 7118, 1191, 796, 187, ...
