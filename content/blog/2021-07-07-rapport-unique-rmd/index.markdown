---
title: "Automatisation des rapports"
subtitle: ""
excerpt: "Pistes pour appliquer le principe DRY !"
date: 2021-07-14
author: "Nicolas Bressoud"
draft: false
images:
series:
tags:
categories:
layout: single
---

DRY : don't repeat yourself.

YAML : params avec les choix.

Bonnes pratiques. etc.

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

