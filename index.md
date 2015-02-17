---
title       : Car mpg analysis app introduction
subtitle    : Assigmnent 2
author      : Bingxin Li
job         : Engineer
framework   : html5slides        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Car mpg analysis app introduction

Purpose

1. Compare linear model between different predictor
2. Display predictor and outcome in plot
3. Show linear model among the plot

--- .class #id 

## How to use
1. Select predictor on the side bar
2. If prefer to draw linear regression model, select "Draw Lm line"
3. The result will display in the main panel. Coefficients start with intercept, followed by slope. Plot is based on selected predictor as x axis and mpg as y axis.

--- .class #id 

## How to get data
The data is based on mtcars built into R package. Use mtcars to retrieve the data. And in this app, we only care about mpg as outcome, hp/cyl/wt as predictor.Below is some biref information about mtcars


```r
data(mtcars)
dim(mtcars)
```

```
## [1] 32 11
```

```r
names(mtcars)
```

```
##  [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
## [11] "carb"
```

--- .class #id 

## How the plot been made
3 types of plot will be generated per predictor selection. mpg ~ cyl, mpg ~ hp or mpg ~ wt. Here we use basic plot

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

--- .class #id 

## How to get linear model
If Draw Lm line has been checked, plot will also contain linear model as green abline


```
## (Intercept)         cyl 
##    37.88458    -2.87579
```

```
## (Intercept)          hp 
## 30.09886054 -0.06822828
```

```
## (Intercept)          wt 
##   37.285126   -5.344472
```

--- .class #id 

## Display linear model on plot
3 types of linear model will be generated per predictor selection. mpg ~ cyl, mpg ~ hp or mpg ~ wt. 

![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png) 

--- .class #id 
