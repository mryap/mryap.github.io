---
#layout: post
title: "Handling Missing Data with Code"
date: 2018-09-16
---

You can leave the data as is and go for a model which can handle missing data
(such as XGBoost, Random Forest).  

For some machine learning algorithms such as Linear Discriminant Analysis
(**LDA**), having missing values in a dataset can cause errors.



### SQL

In SQL, NULL represents a missing or unknown value. You can check for NULL
values using the expression IS NULL. For example, to count the number of
missing birth dates in the people table:

```sql
SELECT COUNT(*) FROM people WHERE birthdate IS NULL;
```



### R
R and ggplot2 subscribes to the philosophy that missing values should never
silently go missing. It’s not obvious where you should plot missing values,
so ggplot2 doesn’t include them in the plot, but it does warn that they’ve been
removed:


- There is a R package dealing with missing data named Amelia
(yes after the famous missing Aviator)

```r
install.packages("Amelia", repos="http://r.iq.harvard.edu", type = "source")
```

### Python

```python
from pandas import read_csv
import numpy
dataset = read_csv('pima-indians-diabetes.csv', header=None)
# mark zero values as missing or NaN
dataset[[1,2,3,4,5]] = dataset[[1,2,3,4,5]].replace(0, numpy.NaN)
# print the first 20 rows of data
print(dataset.head(20))
```
<script src="https://gist.github.com/mryap/d4f092cb2058046ac7e3ba9cc292e74a.js"></script>
