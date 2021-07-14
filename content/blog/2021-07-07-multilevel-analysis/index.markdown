---
title: "Analyses multiniveaux"
subtitle: ""
excerpt: "Notes à moi-même pour comprendre le principe de ce type d'analyses"
date: 2021-07-14
author: "Nicolas Bressoud"
draft: true
images:
series:
tags:
categories:
layout: single
---

On y mettra nos ressources. Nos interprétations.

## Air quality


```r
with(airquality, boxplot(Temp ~ Month))
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-1-1.png" width="672" />



```r
with(airquality, plot(Ozone ~ Temp))
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="672" />


```r
mlev <- levels(with(airquality, as.factor(Month)))
with(airquality, plot(Ozone ~ Temp, 
                      pch = as.numeric(mlev), 
                      col = mlev))
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="672" />

