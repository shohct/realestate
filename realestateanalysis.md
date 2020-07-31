Real Estate Analysis
================
sho
7/28/2020

### Preliminary EDA on real estate data

The data used for this analysis was manually entered by the author
obtained from <https://www.zealty.ca/>.

<table>

<thead>

<tr>

<th style="text-align:right;">

Unit

</th>

<th style="text-align:left;">

Address

</th>

<th style="text-align:right;">

SoldPrice

</th>

<th style="text-align:right;">

AskingPrice

</th>

<th style="text-align:right;">

Bed

</th>

<th style="text-align:right;">

Bath

</th>

<th style="text-align:right;">

Sqft

</th>

<th style="text-align:right;">

Age

</th>

<th style="text-align:left;">

SoldDate

</th>

<th style="text-align:right;">

DaysOnMarket

</th>

<th style="text-align:right;">

PriceSqft

</th>

<th style="text-align:right;">

Floor

</th>

<th style="text-align:right;">

bargaindiff

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:right;">

323

</td>

<td style="text-align:left;">

9288 Odlin Road

</td>

<td style="text-align:right;">

565700

</td>

<td style="text-align:right;">

588000

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

897

</td>

<td style="text-align:right;">

11

</td>

<td style="text-align:left;">

2020-07-13

</td>

<td style="text-align:right;">

6

</td>

<td style="text-align:right;">

630.6577

</td>

<td style="text-align:right;">

3

</td>

<td style="text-align:right;">

22300

</td>

</tr>

<tr>

<td style="text-align:right;">

1205

</td>

<td style="text-align:left;">

7488 Lansdowne Road

</td>

<td style="text-align:right;">

733000

</td>

<td style="text-align:right;">

768000

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

878

</td>

<td style="text-align:right;">

3

</td>

<td style="text-align:left;">

2020-07-17

</td>

<td style="text-align:right;">

21

</td>

<td style="text-align:right;">

834.8519

</td>

<td style="text-align:right;">

12

</td>

<td style="text-align:right;">

35000

</td>

</tr>

<tr>

<td style="text-align:right;">

417

</td>

<td style="text-align:left;">

23233 Gilley Road

</td>

<td style="text-align:right;">

525000

</td>

<td style="text-align:right;">

558888

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

850

</td>

<td style="text-align:right;">

0

</td>

<td style="text-align:left;">

2020-04-01

</td>

<td style="text-align:right;">

160

</td>

<td style="text-align:right;">

617.6471

</td>

<td style="text-align:right;">

4

</td>

<td style="text-align:right;">

33888

</td>

</tr>

<tr>

<td style="text-align:right;">

307

</td>

<td style="text-align:left;">

8033 Saba Road

</td>

<td style="text-align:right;">

595000

</td>

<td style="text-align:right;">

629000

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

862

</td>

<td style="text-align:right;">

10

</td>

<td style="text-align:left;">

2020-07-08

</td>

<td style="text-align:right;">

93

</td>

<td style="text-align:right;">

690.2552

</td>

<td style="text-align:right;">

3

</td>

<td style="text-align:right;">

34000

</td>

</tr>

<tr>

<td style="text-align:right;">

601

</td>

<td style="text-align:left;">

10155 River Drive

</td>

<td style="text-align:right;">

502500

</td>

<td style="text-align:right;">

509000

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

752

</td>

<td style="text-align:right;">

6

</td>

<td style="text-align:left;">

2020-03-10

</td>

<td style="text-align:right;">

7

</td>

<td style="text-align:right;">

668.2181

</td>

<td style="text-align:right;">

6

</td>

<td style="text-align:right;">

6500

</td>

</tr>

</tbody>

</table>

Summary statistics on sold price, asking price, price per sqft, sqft,
age, and \# of days on market were examined and compared between
one-bedroom apartments and two-bedroom apartments.

The plot below shows that while both the asking and sold price of
2-bedroom condos are higher than 1-bedroom condos, when divided by sqft,
the price per sqft is lower for 2-bedroom condos. This is mostly
contributed by 2-bedroom condos having an overall higher square footage
than 1-bedrooms (on average, 2-bedroom condos are 187.17 sqft larger
than 1-bedroom condos.)

    ## $`1`
    ##    SoldPrice       AskingPrice          Bed         Sqft            Age        
    ##  Min.   :357000   Min.   :361800   Min.   :1   Min.   :475.0   Min.   : 0.000  
    ##  1st Qu.:448000   1st Qu.:469000   1st Qu.:1   1st Qu.:591.0   1st Qu.: 1.000  
    ##  Median :508000   Median :526000   Median :1   Median :646.0   Median : 4.000  
    ##  Mean   :507398   Mean   :522629   Mean   :1   Mean   :650.3   Mean   : 7.741  
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

The difference between asking and sold price is investigated further to
identify appropriate negotiation range. Considering there are some new
apartments in the data that could only be sold at asking price, those
were excluded in the following analysis.

Initial review of the data found minimal correlations between different
real estate variables and the bargained difference. The only variable
showing slightly higher correlation is asking price of 2-bedroom condos.

A logarithmic growth between the number of days on market and bargained
difference was noted, where the curve flattens after approximately 30
days on the market. This observation is found for both 1-bedroom and
2-bedroom apartments.

<table>

<thead>

<tr>

<th style="text-align:right;">

Bed

</th>

<th style="text-align:right;">

AvgDiff

</th>

<th style="text-align:right;">

MedianDiff

</th>

<th style="text-align:right;">

MinDiff

</th>

<th style="text-align:right;">

MaxDiff

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:right;">

1

</td>

<td style="text-align:right;">

15403.77

</td>

<td style="text-align:right;">

14450

</td>

<td style="text-align:right;">

\-58000

</td>

<td style="text-align:right;">

137000

</td>

</tr>

<tr>

<td style="text-align:right;">

2

</td>

<td style="text-align:right;">

25377.65

</td>

<td style="text-align:right;">

20500

</td>

<td style="text-align:right;">

\-60000

</td>

<td style="text-align:right;">

144000

</td>

</tr>

</tbody>

</table>

![](realestateanalysis_files/figure-gfm/%7Br%20bargaindiff-1.png)<!-- -->

![](realestateanalysis_files/figure-gfm/marketxdiffplot-1.png)<!-- -->

### Impact of COVID on Real Estate Market

While the data collected from zelaty.ca is not exhaustive of all sales
transactions occurring, a clear decline in the number of sales was
observed starting at week 12 (week of March 16). March 17th marked the
day B.C. declared state of emergency due to COVID-19. Sales transactions
started ot pick up once again around week 20 (week of May 10). This
pattern was not observed in the weekly average sold price. \[test mean
before & after later…\]

![](realestateanalysis_files/figure-gfm/timeseries-1.png)<!-- -->![](realestateanalysis_files/figure-gfm/timeseries-2.png)<!-- -->
