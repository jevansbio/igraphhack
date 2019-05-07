## igraphhack
#### Modification of the plotting code in the igraph R package to accomodate multiple arrow size settings.

By default igraph.plot will only take the first element of a vector for arrow.size and arrow.width arguments. 
This code adds the function igraph.plot2. It is a modificationn of the original igraph.plot to utilise vectors of 

Instructions:
Download the source file
load into R using 

```
source("igraphplot2.R")
```

Add the new functions to the igraph namespace using:

```
environment(plot.igraph2) <- asNamespace('igraph')
environment(igraph.Arrows2) <- asNamespace('igraph')
```

you can now use igraph.plot2 to plot networks with different arrow sizes/widths.
e.g:
```
plot.igraph2(g2,edge.arrow.size=E(g2)$weight/max(E(g2)$weight)/2,edge.arrow.width=E(g2)$weight/max(E(g2)$weight))
```
