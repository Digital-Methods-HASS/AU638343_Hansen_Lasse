---
title: "W4 - Assignment"
author: "Lasse Hansen"
date: "21/09/2021"
output: html_document
---
For this assignment, please answer the following three questions showing your code and results and then take a particular screenshot of your working environment. You can upload here (to Brightspace) the code and the URL to the screenshot OR submit everything to Github and submit here a single link to your repository.

```{r}
pacman::p_load(tidyverse)
```


1) Use R to figure out how many elements in the vector below are greater than 2.

```{r}
rooms <- c(1, 2, 1, 3, 1, NA, 3, 1, 3, 2, 1, NA, 1, 8, 3, 1, 4, NA, 1, 3, 1, 2, 1, 7, 1, NA)
```

#I am using the function subset() to subset all elements that are greater than 2. Thereafter, I am using the function length to count the length of the vector after it being subset.

```{r}
rooms %>% subset(. > 2) %>% length(.)
```

#Which means 8 elements in the vector are greater than two.

2) What type of data is in the 'rooms' vector?

#The data in the rooms vector is numeric.


3) What is the result of running the median() function on the above 'rooms' vector?

#If you just run meadian() without doing anything to cope with NA values you will just get NA out:

```{r}
median(rooms)
```

#However you can add a statement to cope with the NA:

```{r}
median(rooms, na.rm = T)
```

#Which gives 1.5

4) Submit the following image to Github: Inside your R Project (.Rproj), install the 'tidyverse' package and use the download.file() and read_csv() function to read the SAFI_clean.csv dataset into your R project as 'interviews' digital object (see instructions in https://datacarpentry.org/r-socialsci/setup.html and 'Starting with Data' section). Take a screenshot of your RStudio interface showing

a) the line of code you used to create the object,

#Install tidyverse, you can do it with pacman, then you can load and download packages at the same time (saves one line of code), however you need to download pacman first

```{r}
pacman::p_load(tidyverse)
```

#Then i load the csv file directly from github

```{r eval=TRUE, message=FALSE, purl=FALSE}
Safi <- read_csv("https://raw.githubusercontent.com/yorkulibraries/rworkshop/master/SAFI_clean.csv")
```


