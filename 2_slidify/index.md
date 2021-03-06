---
title       : BDP_project-slidify pitch
subtitle    : Checking intervall effect on regression model
author      : Torbjorn Kraft
logo        : ../../img/slidify_logo_big.png
url         :
      assets: ../../assets
job         : Part2-ReproducibleSlidifyPitch
framework   : io2012        # {io2012, html5slides, shower, dzslides, revealjs...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow       # {tomorrow, default...}
widgets     : [bootstrap, quiz, shiny, interactive]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Background 
<p style="font-size:18px">
This is a project to explore usage of the slidify function in R Studio. It's a assignment for a John Hopkins course in Building Data products and will give a pitch to the first part of this assignment that is to develop a simple shiny app. The shiny app will be described later in this presentation.</p>
  

### The Shiny APP
<p style="font-size:18px">
In the Shiny App I wanted to illustrate a possibility to explore the effects on a simple regression model when just studying a selected interval. In the shiny app you can select an interval for one of the variables in the mtcars dataset (qsec) and to observe the difference between the regression slope for this selected interval compared to the regression slope for the full dataset. As regression model for this example a use a well established and used linear regression model (R: lm() ) to illustrate the qsec effects on mpg.</p>
  

--- &twocol
## Dataset description
<p style="font-size:18px">
The dataset used for this project is the famous mtcars, that is a well known dataset for usage in education. For deeper understanding of the dataset please see: https://stat.ethz.ch/R-manual/R-devel/library/datasets/html/mtcars.html The variables that are used here are:
mpg:  miles per US Gallon & qsec: time in seconds for a quarter mile</p>

*** =left
<p style="font-size:14px">
First a look at the full dataset and all the variables</p>

```
## 'data.frame':	32 obs. of  11 variables:
##  $ mpg : num  NULL ...
##  $ cyl : num  NULL ...
##  $ disp: num  NULL ...
##  $ hp  : num  NULL ...
##  $ drat: num  NULL ...
##  $ wt  : num  NULL ...
##  $ qsec: num  NULL ...
##  $ vs  : num  NULL ...
##  $ am  : num  NULL ...
##  $ gear: num  NULL ...
##  $ carb: num  NULL ...
```

*** =right
<p style="font-size:14px">
Then a plot of the variables of interest for this project, with a regression line added: </p>
![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

*** =fullwidth
<p style="font-size:16px">
The variables that are used here are:
mpg:  miles per US Gallon
qsec: time in seconds for a quarter mile
</p>

--- &twocol

## The Shiny App  
 
*** =left
  
https://torkra.shinyapps.io/DDP_project_shinyapps/  
  
  
<p style="font-size:16px">
The overall regression trend is that longer time on the quarter mile (qsec) the higher mpg. But in some selected intervals you might find the this isn't true. You find a flatish trend in the intervals of 18 and above and for example 16-19. And an negative trend for example between 14-18 and 18-25. But as the number of observations are limited you might be careful in making too far conclusions from this. But you might find intresting spots of interval in your dataset.  </p>
  
<p style="font-size:14px">
For exampel: see the shift in the regression line slope for the intervall 18 to 25 compared to the slope for the full dataset on previous slide:  </p>
  
![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 

  
*** =right  
  
<p style="font-size:16px">
When doing exploatory analysis on a new dataset to better understand the data you often also  expriments with using different predictions models. In this specific app we just use a linear regression model to illustrate the linear regression line based on the full dataset compared to a linear regression line based on just the selected interval.
You can see if the regression differs for different intervalls of the qsec variable.

In this app we plot the dataset and you have the posibility to:
</p>
  
<p style="font-size:16px">
* select the qsec for cars in the interval by adjusting the sliders
</p>
  
<p style="font-size:16px">
* select if to draw a regression line based on the full dataset
  or based on the selected intervall by using the radiobuttons
</p>  
  
*** =fullwidth

---

## Conclusion and wraping up  
### Discussion  
<p style="font-size:18px">
When selecting different intervals of a dataset (in this app the mtcars dataset) you can easily see in which interval the slope of the regression model shifts. This can easily be done by switching between full regression model and the regression model for the selected interval. As one example this can be handy for checking the effects of outliers on a regression model.
</p>
  
### Next steps
<p style="font-size:18px">
for this shiny app wil be to add the possibility to switch between even more regression models and to be able to select intervals for both dimensions/variables. The first to better be able to see the effects of using different regression models on the dataset and especially within the selected interval. For the later it would be handy to easily be able to select an interval in both dimensions for example for excluding outliers or a set of observations.
</p>
  
### Improvements
<p style="font-size:18px">
Anohter improvement to this shiny app besides the ones mentioned in the next step section would be to be able to use this for exploring arbitrary data sets.
</p>
