# Graphs-and-Plots
This repository is collection of graphs and plots from web, self-generated, etc. 

#Intro

Here is a really nice website to get tutorials on how to use gglot: http://tutorials.iq.harvard.edu/R/Rgraphics/Rgraphics.html
Here is another one: https://joergsteinkamp.wordpress.com/2016/01/22/broken-axis-with-ggplot2/
Here is another source, it talks about modifying axis: http://www.sthda.com/english/wiki/ggplot2-axis-ticks-a-guide-to-customize-tick-marks-and-labels

#Scatterplot
Note on generating multiple regression lines
# Multiple_regression_lines
Retrieved from:
https://www.r-bloggers.com/multiple-regression-lines-in-ggpairs/


```r
require(datasets)
require(GGally)
require(ggplot2)

my_fn <- function(data, mapping, ...){
  p <- ggplot(data = data, mapping = mapping) + 
    geom_point() + 
    geom_smooth(method=loess, fill="red", color="red", ...) +
    geom_smooth(method=lm, fill="blue", color="blue", ...)
  p
}

ggpairs(data, lower = list(continuous = my_fn))

```
![Image of figure1][figure1]
[figure]: https://github.com/johnypark/Graphs-and-Plots/blob/master/RegressionResult(1).pdf

