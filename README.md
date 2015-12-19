geoaxe
======



[![Build Status](https://travis-ci.org/ropenscilabs/geoaxe.svg)](https://travis-ci.org/ropenscilabs/geoaxe)

`geoaxe` - split geospatial objects into pieces

## Install


```r
devtools::install_github("ropenscilabs/geoaxe")
```


```r
library("geoaxe")
```

## Spatial Polygons and friends input

Works for only `SpatialPolygons` for now, but aim to include related classes soon.


```r
library("rgeos")
wkt <- "POLYGON((-180 -20, -140 55, 10 0, -140 -60, -180 -20))"
poly <- readWKT(wkt)
polys <- chop(x = poly)
```

Plot original polygon


```r
plot(poly, lwd = 6)
```

![plot of chunk unnamed-chunk-5](inst/img/unnamed-chunk-5-1.png) 

Add chopped up polygon bits


```r
plot(polys, add = TRUE)
```

![plot of chunk unnamed-chunk-6](inst/img/unnamed-chunk-6-1.png) 

## Well-Known Text input

"xxx"

## Meta

* Please [report any issues or bugs](https://github.com/ropenscilabs/geoaxe/issues).
* License: MIT
