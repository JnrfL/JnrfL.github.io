---
title       : Developing Data Products Project Pitch
subtitle    : ROAS App
author      : Jean Rafael Angeles
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap]  # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## __Overview__

### _Google Analytics_ is a useful tool that provides you insights for your website. There are two versions currently available. The free standard __Google Analytics(GA)__ and the subscription based __Google Analytics Premium(GAP)__.

--- .class #id 

## __The Problem__

### Sadly GAP is a costly product. It's suited for sites with large traffic. GAP also has analytics features not present in GA. One of such is the _ROI Analysis Tool_.

--- 

## __Here's An Alternative__

### The _ROAS app_ is basically an indepented ROI Analysis Tool. It enables standard GA users to experience the ROI Analysis Tool without the need for GAP subscription.

---

## __Prior Data Cleaning__

Here's a sample of the state the data coming from GA looks like:


```
##   MCF.Channel.Grouping        Spend Conversions Conversion.Value
## 1          Paid Search A$215,093.54         401     A$169,511.05
## 2              Display  A$55,561.20         335      A$16,025.66
## 3       Organic Search  A$16,000.68       1,000      A$15,709.03
## 4               Direct        â???"       1,111   A$1,208,675.71
## 5             Referral        â???"         105     A$911,730.32
## 6              (Other)        â???"           8      A$69,483.56
```

The raw data isn't readily available for the needed computation so data cleaning codes.

---

## __After Data Cleaning__

Here's what the data looks like after cleaning it.


```
##   MCF.Channel.Grouping     Spend Conversions Conversion.Value      ROAS
## 1          Paid Search 215093.54         401        169511.05 0.7880806
## 2              Display  55561.20         335         16025.66 0.2884326
## 3       Organic Search  16000.68        1000         15709.03 0.9817726
## 4               Direct      0.00        1111       1208675.71       Inf
## 5             Referral      0.00         105        911730.32       Inf
## 6              (Other)      0.00           8         69483.56       Inf
```

---

## __Computations__

Here's the computations that has been formatted as well.

__Spend__

```
## [1] "$286,655.4"
```

__Conversions__

```
## [1] "3,020"
```

__Conversion Value__

```
## [1] "$2,440,296"
```

__ROAS__

```
## [1] "8.51%"
```
