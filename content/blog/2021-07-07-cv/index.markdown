---
title: "Gérer mon CV avec Zotero et R"
subtitle: ""
excerpt: "Mise à jour automatique des publications aux normes APA."
date: 2021-07-14
author: "Nicolas Bressoud"
draft: false
images:
series:
tags:
categories:
layout: single
---

L'enjeu sera de produire une liste de publi selon les conventions de CV et pas par défaut (à travailler !).

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

