---
title: "ecosphere_app"
output: 
  html_document: 
    keep_md: yes
date: "2024-03-07"
---




## Load the Libraries

```r
library("tidyverse")
```

```
## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
## ✔ dplyr     1.1.4     ✔ readr     2.1.4
## ✔ forcats   1.0.0     ✔ stringr   1.5.1
## ✔ ggplot2   3.4.4     ✔ tibble    3.2.1
## ✔ lubridate 1.9.3     ✔ tidyr     1.3.0
## ✔ purrr     1.0.2     
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
```

```r
library("janitor")
```

```
## 
## Attaching package: 'janitor'
## 
## The following objects are masked from 'package:stats':
## 
##     chisq.test, fisher.test
```

```r
library("naniar")
library("RColorBrewer")
```

## Load the Data

```r
ecosphere <- read_csv("ecosphere.csv") %>% clean_names() 
```

```
## Rows: 551 Columns: 21
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr (10): Order, Family, Common Name, Scientific Name, Diet, Life Expectancy...
## dbl (11): log10(mass), Mean Eggs per Clutch, Mean Age at Sexual Maturity, Po...
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```
## About our App 
In our app, users will be able to select a habitat location and species to learn more about that species's life history events. The life history events available for users to learn about per species and habitat include: 

Migration/range size, urban tolerance, population size, life expectancy, reproduction rates, log10mass, and diet. 
