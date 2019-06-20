# car-accident-analysis

<p align="center">
<img src="https://github.com/ianjeffries/car-accident-analysis/blob/master/images/uk_accidents.png" alt="Map of Accidents in the UK" width="250" height="430">
</p>

## Index 
1. [Summary](https://github.com/ianjeffries/car-accident-analysis#summary)
2. [File Directory](https://github.com/ianjeffries/car-accident-analysis#file-directory)
3. [Language and Packages Used](https://github.com/ianjeffries/car-accident-analysis#language-and-packages-used)
4. [Installing PySpark](https://github.com/ianjeffries/car-accident-analysis#installing-pyspark)
4. [Credits](https://github.com/ianjeffries/car-accident-analysis#credits)
5. [License](https://github.com/ianjeffries/car-accident-analysis#license)

## Summary 
The following project uses Python and PySpark to simulate how to use big data processing to analyze car crashes in the UK. The following notebook could be used in conjunction with databricks to process the data across a real cluster. 

## File Directory

1. [**data**](https://github.com/ianjeffries/car-accident-analysis/tree/master/data) - contains the four files used in analysis:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [Acc.csv](https://github.com/ianjeffries/car-accident-analysis/blob/master/data/Acc.csv) - 2017 accident data reported by the UK police force.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [Cas.csv](https://github.com/ianjeffries/car-accident-analysis/blob/master/data/Cas.csv) - 2017 casualty data reported by the UK police force.   
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [Veh.csv](https://github.com/ianjeffries/car-accident-analysis/blob/master/data/Veh.csv) - 2017 vehicle data reported by the UK police force.   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [dictionary.xls](https://github.com/ianjeffries/car-accident-analysis/blob/master/data/dictionary.xls) - Data dictionary used to define coded categorical values within datasets.
     
2. [**images**](https://github.com/ianjeffries/car-accident-analysis/tree/master/images) - contains vizualizations:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [uk_accidents.png](https://github.com/ianjeffries/car-accident-analysis/blob/master/images/uk_accidents.png) - Heatmap showing accidents in the UK by accident severity.  
  
3. [**car_crash.ipynb**](https://github.com/ianjeffries/car-accident-analysis/blob/master/car_crash.ipynb) - Jupyter Notebook containing all analysis performed on the datasets, along with vizualizations.  

## Language and Packages Used

Python is used in conjunction with Pyspark for all analysis performed. 

The following commands will import all necessary packages:
  
  ```
import pyspark, os, zipfile
import pandas as pd
import urllib.request
import matplotlib.pyplot as plt
import cartopy.crs as ccrs
from pyspark.sql import SQLContext
from pyspark import SparkContext
from pyspark.sql.types import IntegerType
```

## Installing PySpark

PySpark takes special configuration to install and run within Jupyter Notebook: 

1. If you're using windows, Michael Galarnyk has an excellent [tutorial](https://medium.com/@GalarnykMichael/install-spark-on-windows-pyspark-4498a5d8d66c) on installing PySpark for windows.

2. If you are installing on Linux or Mac OS, Charles Bochet's [article](https://blog.sicara.com/get-started-pyspark-jupyter-guide-tutorial-ae2fe84f594f) will get you started.

## Credits

1. Would like to thank the UK goverment for posting the data on [their website](https://data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data)  
2. Would like to thank the [stackoverflow user](https://stackoverflow.com/questions/39699107/spark-rdd-to-dataframe-python) whose function I stole, because of you lot I get to stand on the shoulders of giants. 

## License 

MIT License
Copyright (c) 2019 Ian Jeffries
