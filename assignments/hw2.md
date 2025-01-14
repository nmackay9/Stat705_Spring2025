---
layout: page
title: HW02 Estimation, Uncertainty
permalink: /assignments/hw2
parent: Assignments
nav_order: 2
---

# Homework 2 **Due Tuesday September 13 at 11:59pm CT**{: .label .label-red }

In an Rmd file, complete the exercises below and knit to pdf or html. Submit the (pdf or html) file to canvas. Please name your file "Assignment2_YourLastName" (e.g., Assignment2_Smith.pdf).
Download template .Rmd [here](https://github.com/jlacasa/stat705_fall2024/blob/main/homeworks/hw2.qmd).

## Exercise 1  
Read the data in the chunk below. Propose a statistical model (using mathematical notation) to describe the relationship between corn yield and plant density, and fit that model to the data.  

```
library(tidyverse)
url <- "https://raw.githubusercontent.com/jlacasa/stat705_fall2024/main/classes/data/corn_example2.csv"
data <- read.csv(url)
data %>% 
  ggplot(aes(plant_density, yield_Mgha))+
  geom_point()+
  labs(x = expression(Plant~Density~(plants~m^{-2})), 
       y = expression(Grain~Yield~(Mg~ha^{-1})))+
  theme_classic()+
  coord_cartesian(xlim = c(0, 15), 
                  ylim = c(0, 16), 
                  expand = F)+
  theme(aspect.ratio = 1)
```

### Answer the following questions:  

a. What is the plant density that maximizes grain yield? Provide a point estimate and some measure of uncertainty.  
b. How much yield do you expect the crop to yield **on average** with 8 plants per m^2? What is a good 95% confidence interval for that value?    

c. What is a reasonable 95% confidence interval for observable yields at 8 plants per m^2?    

d. Which confidence interval would be affected most is the sample size was increased twofold?    

