# First Step
```py
#Get the iris data
!wget http://datachemeng.wp.xdomain.jp/wp-content/uploads/2017/04/iris_withspecies.csv
#check the data
!cat iris.csv
#import csv
f = open('iris.csv')
reader = csv.reader(f)
lines = list(reader)
header, values = lines[0], lines[1:]
data_dict = {h: v for h, v in zip(header, zip(*values))}
from pandas import Series, DataFrame
import pandas as pd
frame = DataFrame(data_dict, dtype=np.float64, columns=header)
```
