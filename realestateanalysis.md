Real Estate Analysis
================
sho
7/28/2020

## Preliminary EDA on real estate data

    ## # A tibble: 389 x 12
    ##     Unit Address SoldPrice AskingPrice   Bed  Bath  Sqft   Age SoldDate
    ##    <dbl> <chr>       <dbl>       <dbl> <dbl> <dbl> <dbl> <dbl> <chr>   
    ##  1   323 9288 O~    565700      588000     2     2   897    11 7/13/20~
    ##  2  1205 7488 L~    733000      768000     2     2   878     3 7/17/20~
    ##  3   417 23233 ~    525000      558888     2     2   850     0 4/1/2020
    ##  4   307 8033 S~    595000      629000     2     2   862    10 7/8/2020
    ##  5   601 10155 ~    502500      509000     2     2   752     6 3/10/20~
    ##  6  1101 8800 H~    771800      799000     2     2   806     0 7/6/2020
    ##  7   501 9399 A~    600000      638000     2     2   821     5 7/6/2020
    ##  8  1707 9188 C~    598000      599000     2     2   809    13 7/9/2020
    ##  9  1708 8833 H~    735000      755000     2     2   822     4 6/28/20~
    ## 10   216 9366 T~    620000      629000     2     2   834     4 7/1/2020
    ## # ... with 379 more rows, and 3 more variables: DaysOnMarket <dbl>,
    ## #   PriceSqft <dbl>, Floor <dbl>

    ## $`1`
    ##    SoldPrice       AskingPrice          Bed         Sqft            Age        
    ##  Min.   : 53900   Min.   :361800   Min.   :1   Min.   :475.0   Min.   : 0.000  
    ##  1st Qu.:448000   1st Qu.:469000   1st Qu.:1   1st Qu.:591.0   1st Qu.: 1.000  
    ##  Median :508000   Median :526000   Median :1   Median :646.0   Median : 4.000  
    ##  Mean   :504831   Mean   :522629   Mean   :1   Mean   :650.3   Mean   : 7.741  
    ##  3rd Qu.:550000   3rd Qu.:570000   3rd Qu.:1   3rd Qu.:711.0   3rd Qu.:12.000  
    ##  Max.   :715900   Max.   :715900   Max.   :1   Max.   :795.0   Max.   :38.000  
    ##   DaysOnMarket      PriceSqft     
    ##  Min.   :  0.00   Min.   : 103.9  
    ##  1st Qu.:  5.00   1st Qu.: 683.5  
    ##  Median : 13.00   Median : 786.8  
    ##  Mean   : 31.15   Mean   : 783.1  
    ##  3rd Qu.: 41.00   3rd Qu.: 895.3  
    ##  Max.   :194.00   Max.   :1058.2  
    ## 
    ## $`2`
    ##    SoldPrice       AskingPrice          Bed         Sqft            Age        
    ##  Min.   :400000   Min.   :438000   Min.   :2   Min.   :709.0   Min.   : 0.000  
    ##  1st Qu.:550000   1st Qu.:573975   1st Qu.:2   1st Qu.:811.0   1st Qu.: 3.000  
    ##  Median :602750   Median :629000   Median :2   Median :845.0   Median : 6.000  
    ##  Mean   :619565   Mean   :645807   Mean   :2   Mean   :837.5   Mean   : 7.855  
    ##  3rd Qu.:675750   3rd Qu.:699900   3rd Qu.:2   3rd Qu.:870.0   3rd Qu.:12.000  
    ##  Max.   :880000   Max.   :989000   Max.   :2   Max.   :900.0   Max.   :38.000  
    ##   DaysOnMarket      PriceSqft     
    ##  Min.   :  0.00   Min.   : 455.1  
    ##  1st Qu.:  9.00   1st Qu.: 664.2  
    ##  Median : 27.00   Median : 727.7  
    ##  Mean   : 43.29   Mean   : 740.5  
    ##  3rd Qu.: 57.75   3rd Qu.: 831.1  
    ##  Max.   :229.00   Max.   :1017.3

![](realestateanalysis_files/figure-gfm/EDA-1.png)<!-- -->
