---
title       : Visualize Your Next Job Application
subtitle    : Word cloud of Job Description and Keyword Match % Calculation
author      : Alicia Brown
job         : Data Science Student, Johns Hopkins University, Coursera.org
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## About

The shiny app, Visualize Your Next Job, allows users to enter a potential job description and important keywords in order to visually see what desired skills, requirements, and other words show up in the job description as well as seeing how closely it matches keywords the job applicant hopes to find in the job.

The wordcloud library generates a text representation of the frequency of terms in  dataset and can be configured to display at minimum frequency level, if so desired by the author.

The barplot also matches any keywords entered by the job seeker and calculates the percentage match on the job description.

---

## The word cloud


```r
library(RColorBrewer); library(wordcloud); library(Rcpp); require(Rcpp) 
wordcloud(words=c('visualize','your','future','job','data'),freq=c(4,2,3,4,5),
          scale=c(5,.15),min.freq=1,random.order=FALSE,rot.per=.15,
          colors=brewer.pal(8,"Accent"),vfont=c("serif","plain"))
```

<img src="figure/unnamed-chunk-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />

---

## The keyword match calculation for keywords "data" and "shiny" on job description terms.
![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2.png) 

---

## Find your Data Scientist dream job at ...

[https://alicia.shinyapps.io/jobwordcloud/](https://alicia.shinyapps.io/jobwordcloud/)

<img src="assets/img/jobwordcloud.jpg" height=400 align="center">
