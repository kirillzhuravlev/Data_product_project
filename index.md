---
title       : Car efficiency prediction
subtitle    : 
author      : Kirill Zhuravlev  
job         : Engineer
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Importance of the problem

 - Car efficiency prediction is important for several groups of people:
 - 1) Self-employed (pizza delivery, newspaper delivery, babysitters, tutors etc.)
 - 2) Frequent travelers (salespersons, advertisers)
 - 3) Small businesses (fast-food, pet grooming, carpet/house cleaning, yard/lawn management, etc.)
 - Costs of fuel are important in planning and managing business, may constitute significant portion of costs
 - How efficient is the car you or your business use? Can we predict it based on its power?
 - Does efficiency depend on the transmission type of your vehicle?
 - We present new algorithm allowing one to predict the car fuel        consumption efficiency (measured in miles per gallon of fuel) if the car power and its transmission type are given.

---

## Data used to build the prediction model

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />
Data was taken from 1974 Motor Trend US magazine. We used simple linear regression model to predict the efficiency of a vehicle based on its power, measured in horsepowers.

---

## Data with the linear regression models

<img src="assets/fig/unnamed-chunk-2-1.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />
Blue and red lines are best linear fits for cars with manual and automatic transmission, respectively.

---

## Web application done using shiny

Below is a screenshot of our web application
<!--html_preserve--><div class="container-fluid">
<h2>
<strong style="color:red">Car efficiency calculator</strong>
</h2>
<div class="row">
<div class="col-sm-4">
<form class="well">
<div class="form-group shiny-input-container">
<label for="hrp">
<p style="color:orange">Power, hp</p>
</label>
<input id="hrp" type="number" class="form-control" value="100" min="0" max="400"/>
</div>
<br/>
<div id="trans" class="form-group shiny-input-radiogroup shiny-input-container">
<label class="control-label" for="trans">
<p>
<em style="color:magenta">Transmission type</em>
</p>
</label>
<div class="shiny-options-group">
<div class="radio">
<label>
<input type="radio" name="trans" value="auto" checked="checked"/>
<span>Automatic</span>
</label>
</div>
<div class="radio">
<label>
<input type="radio" name="trans" value="man"/>
<span>Manual</span>
</label>
</div>
</div>
</div>
<div>
<button type="submit" class="btn btn-primary">Submit</button>
</div>
</form>
</div>
<div class="col-sm-8">
<h3 style="color:blue">Your car efficiency is</h3>
<span id="hrp" class="shiny-text-output"></span>
<h5>
<strong>mpg</strong>
</h5>
</div>
</div>
</div><!--/html_preserve-->

```
## Error in shinyAppDir(x): App dir must contain either app.R or server.R.
```
