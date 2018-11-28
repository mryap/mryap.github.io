---
title: "Working with JSON Data"
date: 2018-11-10
tags: [API, json]
excerpt: "‘jsonlite’ has a function to deal with ‘NDJSON’ file type with ‘stream_in()’ function"
mathjax: "true"
---

Acquire Data

```{r}
library(jsonlite)
yelp <- fromJSON("https://www.dropbox.com/s/gd1k41y9gbpfwq3/yelp_academic_dataset_business.json")
```

```{r}
install.packages('curl')
```
‘jsonlite’ actually has a function to deal with this ‘NDJSON’ file type with ‘stream_in()’ function

need to use ‘file()’ function to create a ‘connection’ for accessing to the files on your disk when you use ‘stream_in()’ function.

53MB JSON data upload to R Studio. To import, add " marks (source: https://stackoverflow.com/questions/2617600/importing-data-from-a-json-file-into-r/50965690#50965690)
```{r}
library(jsonlite)
yelp <- stream_in(file("yelp_academic_dataset_business.json"))
```


```{r}
head(yelp,10)
```
find out how the data has been imported by quickly running ‘str()’ function.
```{r}
str(yelp)
```
use ‘flatten()’ function from ‘jsonlite’ package to make the nested hiearchical data structure into a flatten manner by assigning each of the nested variable as its own column as much as possible.
```{r}
yelp_flat <- flatten(yelp)
str(yelp_flat)
```

to make it easier to see the data frame data in R console UI, use 
use ‘as_data_frame()’ function from the new package called ‘tibble’
```{r}
library(tibble)
yelp_tbl <- as_data_frame(yelp_flat)
yelp_tbl
```


