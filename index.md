---
title       : When will California fall into the Ocean?
subtitle    : A Data Science Class Project
author      : Adam F Clark
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]     # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, draft}
output: html_document
---

## California... When will it go?

- Super Snazzy and Jazzy Inferface!

- You can learn the probability that California will fall into the ocean by a date you specify!

- It slices, it dices, it simply takes the date you specify and the probability of an Earthquake on any given day - and Whoosh!  Math is done!

--- .class #id 

## How to use this tool

1. Go to this site: https://adamfclark.shinyapps.io/DevelopingDataProducts
2. Select a date in the future (the future is so exciting!)
3. Enter the probability that an Earthquake will happen on any given day - don't know?  Neither does the tool!  Just make it up!
4. Click the 'Submit' button
5. Oooh and Aaah over the resulting calculation

--- .class #id 

## What are critics saying about this tool?

1. "Best thing since sliced bread!" - Abraham Lincoln

2. "I didn't know, but now I do!" - Barrack Obama

3. "I was just trying to eat my breakfast in peace." - Dad

4. "I get no respect, I tell ya." - Rodney Dangerfield

--- .class #id 

## Under the covers

- So what does the tool really do?
- Let 'dailyProb' (or p in the equation below) be the probability of the event occuring each day
- Let 'deltaDate' (or d in the equation below) be the number of days in teh future of the specified date
- It simply solves the equation: $1-(1-p)^d$
- Using R, the code looks like this:


```r
dailyProb = 0.01
deltaDate = 20
1-((1-dailyProb)^deltaDate)
```

```
## [1] 0.1820931
```
