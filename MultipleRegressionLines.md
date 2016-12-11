# R_graph
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

