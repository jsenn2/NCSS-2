# Interview Mode Homogeneity
Jeremy Senn

## Purpose

Examine whether the NCSS 2 dataset exhibits statistical heterogeneity
based on the interview mode (`ITWMETHOD` variable).

## Procedure

The dataset was filtered to include only observations from the second
wave, which is the sole wave incorporating both CAWI and CATI interview
methods. Each numeric and binary variable was subjected to regression
analysis, using `ITWMETHOD` as the independent variable. Detailed
specifications and outcomes of these regression models are stored in the
`mode_homogeneity.RDS` file within this repository.

## Results

A total of 154 variables were analyzed. In this analysis, `ITWMETHOD`
emerged as a statistically significant predictor for 19 variables.
Ordered by ascending p-values associated with the `ITWMETHOD` predictor,
these variables are:

`OTHLANG` `REFWOR` `SERMTIME` `CATHWOR` `EVANWOR` `BOARDNUM` `MBRCOHBT`
`UPFUSION` `GRNGRP` `MBRALCMD` `GRNRG` `GRNAWR` `CLS13_14W2` `STRGPLAN`
`MUSLMWOR` `BOARDGEN` `PIANO` `NEWMEMS` `GRNWSHP`

Comprehensive outputs of the regression models (also sorted by the
`ITWMETHOD`’s p-value) are presented towards the end of this report.

## Conclusion

Given the significant influence of the measurement mode on the
aforementioned variables, it is advisable to account for the mode effect
in subsequent data analyses.

## Models output

``` r
library(tidyverse)
read_rds("mode_homogeneity.RDS")
```

    $OTHLANG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.787    0.0670     11.7  7.17e-32
    2 ITWMETHODCAWI   -0.675    0.126      -5.38 7.65e- 8

    $REFWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.18     0.0732    -16.1  1.85e-58
    2 ITWMETHODCAWI   -0.545    0.165      -3.30 9.50e- 4

    $SERMTIME
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      22.9      0.664     34.4  6.53e-185
    2 ITWMETHODCAWI     4.03     1.30       3.10 2.00e-  3

    $CATHWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.924    0.0688    -13.4  4.44e-41
    2 ITWMETHODCAWI   -0.452    0.149      -3.04 2.37e- 3

    $EVANWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.76     0.0878    -20.1  1.12e-89
    2 ITWMETHODCAWI   -0.590    0.207      -2.84 4.45e- 3

    $BOARDNUM
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      6.73      0.153     43.9  3.93e-256
    2 ITWMETHODCAWI    0.798     0.298      2.67 7.57e-  3

    $MBRCOHBT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.83     0.0910     20.1  9.02e-90
    2 ITWMETHODCAWI   -0.423    0.167      -2.53 1.15e- 2

    $UPFUSION
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.01      0.162      6.25 4.19e-10
    2 ITWMETHODCAWI   -0.773     0.308     -2.51 1.21e- 2

    $GRNGRP
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.15     0.0729    -15.8  3.19e-56
    2 ITWMETHODCAWI   -0.402    0.162      -2.48 1.31e- 2

    $MBRALCMD
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      2.98      0.146     20.4  4.35e-92
    2 ITWMETHODCAWI   -0.609     0.246     -2.48 1.33e- 2

    $GRNRG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.04     0.0732    -14.2  1.66e-45
    2 ITWMETHODCAWI    0.338    0.143       2.37 1.78e- 2

    $GRNAWR
    # A tibble: 2 × 5
      term          estimate std.error statistic       p.value
      <chr>            <dbl>     <dbl>     <dbl>         <dbl>
    1 (Intercept)     -0.384    0.0640     -6.00 0.00000000199
    2 ITWMETHODCAWI   -0.292    0.130      -2.26 0.0241       

    $CLS13_14W2
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.706    0.0662     10.7  1.38e-26
    2 ITWMETHODCAWI    0.304    0.137       2.22 2.62e- 2

    $STRGPLAN
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.27      0.107     21.3  1.55e-100
    2 ITWMETHODCAWI    0.554     0.254      2.19 2.89e-  2

    $MUSLMWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      -3.48     0.182    -19.1  3.15e-81
    2 ITWMETHODCAWI    -1.29     0.608     -2.12 3.38e- 2

    $BOARDGEN
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.90     0.0857     33.8  1.08e-178
    2 ITWMETHODCAWI    0.354    0.166       2.12 3.38e-  2

    $PIANO
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.808    0.0672    -12.0  2.67e-33
    2 ITWMETHODCAWI    0.263    0.129       2.04 4.12e- 2

    $NEWMEMS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.808    0.0673    -12.0  3.13e-33
    2 ITWMETHODCAWI   -0.290    0.142      -2.04 4.13e- 2

    $GRNWSHP
    # A tibble: 2 × 5
      term          estimate std.error statistic    p.value
      <chr>            <dbl>     <dbl>     <dbl>      <dbl>
    1 (Intercept)     -0.302    0.0632     -4.79 0.00000167
    2 ITWMETHODCAWI   -0.251    0.127      -1.97 0.0484    

    $LOCSERV
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.16     0.0640     33.8  4.68e-182
    2 ITWMETHODCAWI   -0.243    0.126      -1.93 5.43e-  2

    $NUMATTND
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      63.1       2.43     26.0  1.95e-121
    2 ITWMETHODCAWI     9.27      4.82      1.93 5.44e-  2

    $CLERGRAD
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.458    0.0664      6.90 5.32e-12
    2 ITWMETHODCAWI   -0.243    0.131      -1.86 6.29e- 2

    $RECRCONF
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    0.00388    0.0623    0.0623  0.950 
    2 ITWMETHODCAWI  0.233      0.126     1.85    0.0645

    $JEWWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      -3.83     0.215    -17.8  9.25e-71
    2 ITWMETHODCAWI    -1.35     0.741     -1.82 6.92e- 2

    $WEBSITE
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.20      0.104     21.2  4.49e-100
    2 ITWMETHODCAWI    0.425     0.235      1.81 7.09e-  2

    $LT35PCT
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      20.0      0.516     38.7  1.10e-219
    2 ITWMETHODCAWI    -1.87     1.04      -1.79 7.37e-  2

    $KIDCLASS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.35     0.0769     17.6  4.61e-69
    2 ITWMETHODCAWI    0.286    0.163       1.76 7.88e- 2

    $GT60PCT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      49.0      0.802     61.1   0     
    2 ITWMETHODCAWI     2.82     1.62       1.74  0.0829

    $SERMON
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.47      0.116     21.3  6.04e-101
    2 ITWMETHODCAWI    0.461     0.268      1.72 8.53e-  2

    $ROBE
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     -0.126    0.0622     -2.02  0.0437
    2 ITWMETHODCAWI    0.210    0.123       1.71  0.0880

    $STAFFWMPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      46.8       1.14     41.1  8.74e-216
    2 ITWMETHODCAWI     3.76      2.26      1.67 9.60e-  2

    $HAVEDEN
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      2.59      0.122     21.2  2.17e-99
    2 ITWMETHODCAWI    0.470     0.283      1.66 9.71e- 2

    $WOMGRP
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      0.261    0.0627      4.16 0.0000325
    2 ITWMETHODCAWI    0.204    0.128       1.60 0.110    

    $CVDBFINCOM
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    410677.    45969.      8.93 3.68e-18
    2 ITWMETHODCAWI -141294.    91609.     -1.54 1.23e- 1

    $BUDWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      -4.29     0.269    -16.0  2.76e-57
    2 ITWMETHODCAWI    -1.58     1.04      -1.53 1.27e- 1

    $BAPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      21.9      0.669     32.7  3.53e-165
    2 ITWMETHODCAWI    -2.10     1.38      -1.53 1.27e-  1

    $XOTHWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -3.83      0.215    -17.8  9.25e-71
    2 ITWMETHODCAWI   -0.938     0.619     -1.52 1.29e- 1

    $FEMPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      61.4      0.441    139.     0    
    2 ITWMETHODCAWI    -1.33     0.892     -1.49   0.137

    $NUMTOTAL
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      388.       25.2     15.4  1.71e-49
    2 ITWMETHODCAWI     71.8      50.4      1.43 1.54e- 1

    $CLERGYOU
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.86     0.0912     20.4  7.15e-93
    2 ITWMETHODCAWI   -0.237    0.170      -1.39 1.64e- 1

    $SOCNETACT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    -0.0564    0.0624    -0.904   0.366
    2 ITWMETHODCAWI  -0.169     0.124     -1.37    0.171

    $RELOBJECTS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.15     0.0726    -15.8  3.32e-56
    2 ITWMETHODCAWI   -0.205    0.150      -1.36 1.73e- 1

    $MBRGAY
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.15     0.0755     15.2  4.81e-52
    2 ITWMETHODCAWI   -0.200    0.148      -1.35 1.78e- 1

    $GENDERSEP
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -3.32      0.170    -19.6  1.68e-85
    2 ITWMETHODCAWI    0.397     0.295      1.35 1.79e- 1

    $ORGAN
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.537    0.0643     -8.34 7.30e-17
    2 ITWMETHODCAWI    0.168    0.125       1.34 1.79e- 1

    $EURNOCHPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      22.0      0.750     29.3  1.04e-143
    2 ITWMETHODCAWI     2.08     1.55       1.34 1.80e-  1

    $OTHTRAD
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.418    0.0637     -6.56 5.46e-11
    2 ITWMETHODCAWI   -0.175    0.130      -1.34 1.80e- 1

    $POLITICS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.698    0.0663    -10.5  6.64e-26
    2 ITWMETHODCAWI   -0.180    0.134      -1.34 1.81e- 1

    $RICHFAITH
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.71     0.0879    -19.4  7.07e-84
    2 ITWMETHODCAWI   -0.244    0.184      -1.33 1.84e- 1

    $FOUNDED
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     1876.       5.55    338.     0    
    2 ITWMETHODCAWI     15.0     11.4       1.31   0.189

    $SWISSPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      68.6      0.846     81.1    0    
    2 ITWMETHODCAWI    -2.25     1.73      -1.30   0.193

    $OUTUPWMSTF
    # A tibble: 2 × 5
      term          estimate std.error statistic    p.value
      <chr>            <dbl>     <dbl>     <dbl>      <dbl>
    1 (Intercept)       2.68     0.454      5.90 0.00000105
    2 ITWMETHODCAWI     1.49     1.13       1.32 0.195     

    $NGRNWSHP
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      4.70      0.294     16.0  2.67e-47
    2 ITWMETHODCAWI   -0.785     0.609     -1.29 1.98e- 1

    $VLTRS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      69.1       3.23     21.4  1.40e-87
    2 ITWMETHODCAWI    -8.14      6.35     -1.28 2.00e- 1

    $CATCHWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -3.79      0.211    -18.0  3.99e-72
    2 ITWMETHODCAWI   -0.693     0.545     -1.27 2.04e- 1

    $POLSENSIB
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.673    0.0659    -10.2  1.73e-24
    2 ITWMETHODCAWI   -0.168    0.133      -1.26 2.08e- 1

    $LDRCOHBT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.797    0.0694     11.5  1.60e-30
    2 ITWMETHODCAWI   -0.169    0.136      -1.24 2.15e- 1

    $GRNSTRIKE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -2.96      0.144    -20.6  4.20e-94
    2 ITWMETHODCAWI   -0.400     0.327     -1.22 2.21e- 1

    $STAND
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -2.09     0.0997    -21.0  1.09e-97
    2 ITWMETHODCAWI   -0.255    0.213      -1.20 2.30e- 1

    $WMVLTRS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      43.9       2.15     20.4  2.01e-80
    2 ITWMETHODCAWI    -5.05      4.23     -1.19 2.33e- 1

    $NUMADLTS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)       99.5      4.81     20.7  1.70e-82
    2 ITWMETHODCAWI     11.5      9.77      1.17 2.41e- 1

    $CVCONTACT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      2.97      0.145     20.5  2.13e-93
    2 ITWMETHODCAWI    0.380     0.328      1.16 2.46e- 1

    $MERGE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.84     0.0904    -20.3  7.75e-92
    2 ITWMETHODCAWI    0.197    0.170       1.16 2.46e- 1

    $TONGUES
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -2.02      0.109    -18.5  1.26e-76
    2 ITWMETHODCAWI    0.231     0.199      1.16 2.47e- 1

    $CATHMVT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      17.6       1.56     11.3  5.39e-23
    2 ITWMETHODCAWI    -3.95      3.43     -1.15 2.50e- 1

    $RECRVISIT
    # A tibble: 2 × 5
      term          estimate std.error statistic     p.value
      <chr>            <dbl>     <dbl>     <dbl>       <dbl>
    1 (Intercept)     -0.328    0.0633     -5.19 0.000000213
    2 ITWMETHODCAWI   -0.147    0.128      -1.14 0.253      

    $GRNAWRBG
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    2015.       0.545   3701.     0    
    2 ITWMETHODCAWI    -1.26     1.14      -1.10   0.271

    $MENGRP
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.768    0.0669    -11.5  1.62e-30
    2 ITWMETHODCAWI    0.146    0.133       1.10 2.72e- 1

    $YTHGRP
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      0.176    0.0624      2.82 0.00473
    2 ITWMETHODCAWI    0.136    0.124       1.10 0.273  

    $OTHGRPS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.693    0.0658    -10.5  6.46e-26
    2 ITWMETHODCAWI    0.136    0.128       1.06 2.90e- 1

    $CHORUS
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    -0.0853    0.0623     -1.37   0.171
    2 ITWMETHODCAWI   0.132     0.125       1.06   0.290

    $IMPNUMREGLR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      145.       6.96     20.9  1.88e-84
    2 ITWMETHODCAWI     14.5     13.8       1.05 2.94e- 1

    $TRADWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.240    0.0627      3.82 0.000133
    2 ITWMETHODCAWI    0.131    0.125       1.05 0.296   

    $OUTUPSTF
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     -0.534     0.176     -3.03 0.00246
    2 ITWMETHODCAWI   -0.447     0.429     -1.04 0.297  

    $BLDGTYPE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.797    0.0672     11.8  2.16e-32
    2 ITWMETHODCAWI    0.139    0.136       1.03 3.04e- 1

    $PLNTCONG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.89     0.0920   -20.5   2.86e-93
    2 ITWMETHODCAWI    0.170    0.174      0.979 3.28e- 1

    $NUMSERV1
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      3.17      0.157    20.2   5.72e-80
    2 ITWMETHODCAWI    0.295     0.309     0.957 3.39e- 1

    $HINDWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -4.45      0.290   -15.3   5.55e-53
    2 ITWMETHODCAWI   -0.730     0.766    -0.954 3.40e- 1

    $WMNBRD
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.41      0.113    21.2   4.19e-100
    2 ITWMETHODCAWI    0.221     0.244     0.907 3.64e-  1

    $RTENURE
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)   2006.        0.444  4523.      0    
    2 ITWMETHODCAWI   -0.796     0.880    -0.904   0.366

    $WMNTCH
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      2.69      0.128    21.0   1.67e-97
    2 ITWMETHODCAWI    0.252     0.280     0.900 3.68e- 1

    $APPLAUSE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -0.430    0.0636    -6.76  1.43e-11
    2 ITWMETHODCAWI   -0.114    0.127     -0.899 3.69e- 1

    $OFS6
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)    169140.     3958.    42.7   1.08e-255
    2 ITWMETHODCAWI   -6996.     7823.    -0.894 3.71e-  1

    $OFS4
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     1691.       39.6    42.7   1.08e-255
    2 ITWMETHODCAWI    -70.0      78.2    -0.894 3.71e-  1

    $OUTUPFTSTF
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      1.10      0.422     2.60   0.0137
    2 ITWMETHODCAWI   -0.930     1.05     -0.887  0.381 

    $DISCRIM
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.94     0.0949   -20.4   1.47e-92
    2 ITWMETHODCAWI    0.148    0.179      0.831 4.06e- 1

    $UPNUMBER
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      3.89      0.278    14.0   1.18e-33
    2 ITWMETHODCAWI   -0.474     0.571    -0.830 4.07e- 1

    $WMNLEAD
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.535    0.0656     8.16  3.35e-16
    2 ITWMETHODCAWI    0.108    0.134      0.806 4.20e- 1

    $POORPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      6.10      0.308    19.8   6.78e-75
    2 ITWMETHODCAWI   -0.541     0.671    -0.806 4.21e- 1

    $YTHMNSTR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     0.398     0.0633     6.29  3.17e-10
    2 ITWMETHODCAWI  -0.0991    0.124     -0.797 4.25e- 1

    $RITGEST
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    -0.112     0.0622    -1.80   0.0717
    2 ITWMETHODCAWI  -0.0983    0.124     -0.794  0.427 

    $COMNGO
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     -2.27      0.107   -21.2   6.75e-100
    2 ITWMETHODCAWI   -0.178     0.224    -0.792 4.28e-  1

    $FTSTAFF
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.24     0.0895    13.8   4.01e-40
    2 ITWMETHODCAWI    0.145    0.184      0.790 4.30e- 1

    $RECYCLE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      0.776    0.0676    11.5   1.65e-30
    2 ITWMETHODCAWI    0.101    0.135      0.753 4.52e- 1

    $LDRALCMD
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.71     0.0884    19.4   7.53e-84
    2 ITWMETHODCAWI   -0.124    0.174     -0.716 4.74e- 1

    $ORTHWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -3.39      0.174   -19.4   5.87e-84
    2 ITWMETHODCAWI   -0.270     0.380    -0.709 4.78e- 1

    $LRNLANG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -1.64     0.0841   -19.4   3.16e-84
    2 ITWMETHODCAWI    0.118    0.167      0.708 4.79e- 1

    $MEDITATE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      1.22     0.0740    16.4   8.41e-61
    2 ITWMETHODCAWI    0.104    0.150      0.698 4.85e- 1

    $NUMREGLR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     142.        6.92    20.5   1.11e-81
    2 ITWMETHODCAWI     9.41     13.9      0.679 4.97e- 1

    $GRNREL
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     0.456     0.0645     7.07  1.54e-12
    2 ITWMETHODCAWI  -0.0812    0.126     -0.643 5.20e- 1

    $LENGTH
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      83.0       1.46    56.8     0    
    2 ITWMETHODCAWI    -1.83      2.90    -0.632   0.527

    $CLERBUDG
    # A tibble: 2 × 5
      term          estimate std.error statistic     p.value
      <chr>            <dbl>     <dbl>     <dbl>       <dbl>
    1 (Intercept)     0.322     0.0644     5.00  0.000000573
    2 ITWMETHODCAWI   0.0762    0.128      0.596 0.551      

    $ADVERT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -0.960     0.0695   -13.8   2.31e-43
    2 ITWMETHODCAWI   0.0797    0.137      0.583 5.60e- 1

    $INSTMENT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.04      0.0707    14.7   4.65e-49
    2 ITWMETHODCAWI   0.0810    0.142      0.569 5.69e- 1

    $OVERHEAD
    # A tibble: 2 × 5
      term          estimate std.error statistic    p.value
      <chr>            <dbl>     <dbl>     <dbl>      <dbl>
    1 (Intercept)    -0.291     0.0627    -4.64  0.00000349
    2 ITWMETHODCAWI   0.0704    0.124      0.569 0.570     

    $CLERGAGE
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     53.6       0.350   153.      0    
    2 ITWMETHODCAWI   -0.378     0.697    -0.543   0.587

    $CVDWSHP
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     0.819     0.0677    12.1   1.27e-33
    2 ITWMETHODCAWI   0.0703    0.135      0.522 6.02e- 1

    $DRUMS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.94      0.0938   -20.7   1.95e-95
    2 ITWMETHODCAWI  -0.0985    0.191     -0.516 6.06e- 1

    $TRAD6
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.64      0.0841   -19.5   1.72e-84
    2 ITWMETHODCAWI  -0.0873    0.170     -0.514 6.07e- 1

    $WMNVLTR
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)      2.25      0.106    21.2   9.79e-100
    2 ITWMETHODCAWI    0.108     0.221     0.489 6.25e-  1

    $OFFMBRLIST
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.55      0.0818    18.9   6.81e-80
    2 ITWMETHODCAWI   0.0705    0.164      0.429 6.68e- 1

    $PARISHW2
    # A tibble: 2 × 5
      term          estimate std.error statistic      p.value
      <chr>            <dbl>     <dbl>     <dbl>        <dbl>
    1 (Intercept)    -0.359     0.0631    -5.69  0.0000000130
    2 ITWMETHODCAWI   0.0533    0.124      0.428 0.669       

    $CLERFORM
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)      0.416     0.231     1.80   0.0721
    2 ITWMETHODCAWI   -0.193     0.451    -0.428  0.669 

    $EMAIL
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.86      0.0909    20.4   9.80e-93
    2 ITWMETHODCAWI   0.0768    0.184      0.419 6.76e- 1

    $GRNELEC
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)   -0.00480    0.0693   -0.0693   0.945
    2 ITWMETHODCAWI -0.0597     0.145    -0.413    0.680

    $RICHPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     20.5       0.966    21.2   9.36e-78
    2 ITWMETHODCAWI    0.874     2.12      0.412 6.81e- 1

    $NUMOFFMBR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1394.       99.6    14.0   4.17e-41
    2 ITWMETHODCAWI    -81.0     199.     -0.408 6.84e- 1

    $JUMP
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)    -2.58       0.121   -21.3   2.24e-100
    2 ITWMETHODCAWI   0.0906     0.234     0.387 6.99e-  1

    $TEENRGLR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      23.2       1.35    17.1   1.56e-59
    2 ITWMETHODCAWI    -1.02      2.68    -0.381 7.03e- 1

    $FTSTAFFWM
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     0.369     0.0514     7.18  1.32e-12
    2 ITWMETHODCAWI   0.0386    0.106      0.366 7.15e- 1

    $GONG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -4.54      0.303   -15.0   1.22e-50
    2 ITWMETHODCAWI   -0.234     0.654    -0.358 7.20e- 1

    $BELLS
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     -4.54      0.303   -15.0   1.22e-50
    2 ITWMETHODCAWI   -0.234     0.654    -0.358 7.20e- 1

    $CLERGONE
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     2.58       0.121    21.2   3.34e-100
    2 ITWMETHODCAWI  -0.0794     0.234    -0.339 7.35e-  1

    $WMNPRCH
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.31      0.0770    17.1   2.15e-65
    2 ITWMETHODCAWI   0.0526    0.157      0.335 7.38e- 1

    $MUSICMIN
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     22.9       0.595    38.5   5.15e-221
    2 ITWMETHODCAWI   -0.385     1.19     -0.325 7.46e-  1

    $GRNPUB
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.66      0.0855   -19.4   4.95e-84
    2 ITWMETHODCAWI  -0.0551    0.171     -0.323 7.47e- 1

    $BRDGENPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     43.5       0.795    54.8     0    
    2 ITWMETHODCAWI    0.499     1.55      0.323   0.747

    $SIGNTURE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.80      0.0893   -20.1   4.02e-90
    2 ITWMETHODCAWI  -0.0571    0.179     -0.319 7.50e- 1

    $SIZECOM
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     53171.     3054.    17.4   1.42e-61
    2 ITWMETHODCAWI    1904.     6043.     0.315 7.53e- 1

    $STAFFGEN
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)      3.88      0.202    19.2   4.70e-71
    2 ITWMETHODCAWI    0.118     0.412     0.285 7.76e- 1

    $STFTWMPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     19.9        1.45    13.8   5.07e-38
    2 ITWMETHODCAWI    0.827      2.93     0.282 7.78e- 1

    $CLERSLRY
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     62951.     1702.    37.0   1.24e-197
    2 ITWMETHODCAWI    -891.     3495.    -0.255 7.99e-  1

    $LAUGH
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     0.121     0.0626     1.94   0.0528
    2 ITWMETHODCAWI  -0.0308    0.123     -0.249  0.803 

    $LDRGAY
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     0.293     0.0668     4.38  0.0000118
    2 ITWMETHODCAWI  -0.0304    0.134     -0.226 0.821    

    $RECRUIT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.82      0.0898    20.3   2.01e-91
    2 ITWMETHODCAWI  -0.0362    0.176     -0.206 8.37e- 1

    $SPONPRAY
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.22      0.0741   -16.5   2.70e-61
    2 ITWMETHODCAWI  -0.0277    0.148     -0.188 8.51e- 1

    $STAFFNUM
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     5.05       0.237    21.3   1.90e-87
    2 ITWMETHODCAWI  -0.0693     0.467    -0.148 8.82e- 1

    $WSHPWEB
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     0.103     0.0657     1.57    0.116
    2 ITWMETHODCAWI  -0.0189    0.128     -0.148   0.882

    $GUITAR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.14      0.0724   -15.7   1.22e-55
    2 ITWMETHODCAWI   0.0202    0.143      0.141 8.88e- 1

    $UPNUMBERcorr
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     4.30       0.306    14.1   3.42e-33
    2 ITWMETHODCAWI  -0.0836     0.638    -0.131 8.96e- 1

    $SOCLSERV
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.60      0.0831    19.2   1.75e-82
    2 ITWMETHODCAWI   0.0205    0.165      0.124 9.01e- 1

    $INVITE
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     0.927     0.0691    13.4   5.19e-41
    2 ITWMETHODCAWI  -0.0170    0.138     -0.123 9.02e- 1

    $GRNSERMON
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.40      0.0782    17.9   1.08e-71
    2 ITWMETHODCAWI   0.0187    0.155      0.120 9.04e- 1

    $CVSUPPRT
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)     1.08      0.0720    15.1   3.15e-51
    2 ITWMETHODCAWI  -0.0158    0.142     -0.111 9.11e- 1

    $INCOME
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    428288.    31704.    13.5   1.39e-37
    2 ITWMETHODCAWI   -6367.    62935.    -0.101 9.19e- 1

    $GRNORGXCHNG
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    -1.14      0.0728  -15.6    3.48e-55
    2 ITWMETHODCAWI  -0.0128    0.144    -0.0887 9.29e- 1

    $CLERWKPCT
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)     71.2        1.06   67.0      0    
    2 ITWMETHODCAWI   -0.188      2.16   -0.0872   0.931

    $SINGING
    # A tibble: 2 × 5
      term          estimate std.error statistic   p.value
      <chr>            <dbl>     <dbl>     <dbl>     <dbl>
    1 (Intercept)     2.26       0.106   21.3    1.16e-100
    2 ITWMETHODCAWI   0.0140     0.211    0.0663 9.47e-  1

    $JOINTWOR
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    0.901      0.0686   13.1    2.08e-39
    2 ITWMETHODCAWI -0.00609    0.136    -0.0449 9.64e- 1

    $EVNGLCAL
    # A tibble: 2 × 5
      term          estimate std.error statistic  p.value
      <chr>            <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    18.5         1.10   16.9    2.27e-45
    2 ITWMETHODCAWI  -0.0861      2.29   -0.0376 9.70e- 1

    $TRAD3
    # A tibble: 2 × 5
      term          estimate std.error statistic p.value
      <chr>            <dbl>     <dbl>     <dbl>   <dbl>
    1 (Intercept)    0.143      0.0622    2.29    0.0217
    2 ITWMETHODCAWI -0.00254    0.123    -0.0206  0.984 

    $CONGREAD
    # A tibble: 2 × 5
      term           estimate std.error statistic  p.value
      <chr>             <dbl>     <dbl>     <dbl>    <dbl>
    1 (Intercept)    0.711       0.0660  10.8     5.32e-27
    2 ITWMETHODCAWI -0.000442    0.131   -0.00338 9.97e- 1
