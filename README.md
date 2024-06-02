# week-2-assignment
#question 1
title: "ANA 515 Assignment 1"
author: "XiaoqiongChen"
date: "2024"
output: "html_document"
theme:"Journal"
---
install.packages("bslib")
#question 2
```{r echo = FAULSE}
#question 3 
install.packages("tidyverse")
install.packages("knitr")
install.packages("bslib")
library(tidyverse)
library(knitr)
library(bslib)
#question 4 
url <- "https://raw.githubusercontent.com/fivethirtyeight/data/master/fifa/fifa_countries_audience.csv"
population_share <- read.csv(url)
#question 5 
filtered <- filter(population_share,population_share <= 1.0)
#question 6
summary(population_share)
#question 7
```{r include = FAULSE}
#question 8
```{r filtered-dist, echo = FAULSE} 
ggplot(filtered, aes(population_share))+
geom_histogram(color="white")```
#question9 
#gdp_weighted_share
ggplot(population_share, aes(population_share)) +  
  geom_bar() +  
  labs(title = "GDP_Weighted",
       x = "GDP")
