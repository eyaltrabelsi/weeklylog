# weeklylog 25.02.2017 - 28.02.2017

## Articles
- [Convert string date to timestamp in Python](http://stackoverflow.com/questions/9637838/convert-string-date-to-timestamp-in-python) `data engineering` `timestamp` `python`
- [Engineers Shouldn’t Write ETL: A Guide to Building a High Functioning Data Science Department](http://multithreaded.stitchfix.com/blog/2016/03/16/engineers-shouldnt-write-etl/) `data engineering` `data science`
- [Debugging Neural Netweorks: A Checklist](https://engineering.semantics3.com/2016/10/09/debugging-neural-networks-a-checklist/) `favorite` `data science` `neural network` `ml` `debugging`
- [Nick Evans: Realtime Risk Management Using Kafka, Python, and Spark Streaming](https://www.youtube.com/watch?v=5XB-T4hzV00&t=1644s) `data engineering` `kafka` `python` `spark`
- [Scope the Solution before Solving the Machine Learning](https://medium.com/dia-co-engineering/scope-the-solution-before-solving-the-machine-learning-7e5ddb622733#.ljbnzjd16) `data science` `ml` 
- [Why pandas users should be excited about Apache Arrow](http://wesmckinney.com/blog/pandas-and-apache-arrow/) `favorite` `data engineering` `apache arrow`
- [Data Wrangling: Clean, Transform, Merge, Reshape](http://nbviewer.jupyter.org/github/pydata/pydata-book/blob/master/ch07.ipynb) `data engineering` `data science` `clean` `transform` `data wrangling`
- [Feather: it's about metadata](http://wesmckinney.com/blog/feather-its-the-metadata/) `data engineering` `feather` `apache arrow`
- [50 things I learned at NIPS 2016](https://blog.ought.com/nips-2016-875bb8fadb8c#.jsg8jhtxo) `favorite` `data science`
- [Serializing Python Objects](http://www.diveintopython3.net/serializing.html) `favorite` `python` `serialization`
- [Basic Mistakes in Database Testing](https://dzone.com/articles/basic-mistakes-database) `data engineering` `testing` `database`
- [Data validation in Python with voluptuous](https://julien.danjou.info/blog/2015/python-schema-validation-voluptuous) `data engineering` `data science` `data validation` `voluptuous`


## Videos
- [A Practical Guide: Building your BI Business Case for 2017](https://www.brighttalk.com/webcast/9059/234889?utm_campaign=knowledge-feed&utm_content=&utm_source=brighttalk-portal&utm_medium=web&utm_term=) `favorite` `bi` `business understanding`
- [The Big BI Dilemma - Bimodal Logical Data Warehouse to the Rescue!](https://www.brighttalk.com/webcast/9059/213223?utm_campaign=knowledge-feed&utm_content=&utm_source=brighttalk-portal&utm_medium=web&utm_term=) `data warehouse` `bi` `dilemma`


## Packages
- [Lightweight, extensible data validation library for Python](https://github.com/nicolaiarocci/cerberus) `python` `data validation`
- [Check syntax of postgresql sql files](https://github.com/markdrago/pgsanity) `postgresql` `syntax checker`
- [Command line utilities for data analysis] (http://github.com/bitly/data_hacks) `cmd` `analysis`
- [Generate and work with holidays in Python](https://github.com/ryanss/python-holidays) `python` `holiday` `timestamp` `feature enrichment`
- [An asynchronous library for accessing mongo with tornado.ioloop http://github.com/bitly/asyncmongo](https://github.com/bitly/asyncmongo) `python` `async` `mongodb`
- [A library for reading text files over multiple cores](https://github.com/wiseio/paratext) `python` `fast` `parallel` `reading` `csv`


## Tips
- **when approaching new data science task we should first**:
	- understand what is the actual goal
	- understand what type of output do i need to achieve this goal
	- understand which types of model produce this desired output
	- understand which types of input would help me produce this desired output
	- understand are theses valid input	  
- **ensuring auto-encoders  does not learn the identity function by**:
    - create some random noise to the data which will "force" the neural network to "understand" the features
- **hdf5 info**:
	- hdf5 has a fair amount of overhead with really small sizes (even 300k enteries is on the smaller size). the folowwing is with no compression on either side. floats are really more efficiently represented in binary. in addition,hdf5 is row based you get much efficiency by having tables that are not too wide but faily long.
	10m+ time can be ms , and 10g will take few seconds.
- **Data quality principles**:
    - understand your data before cleaning improve the efficiently.
    - you can also use combination of fields for data checking. this is sometimes actually necessary because you have to look at all the fieldstogether to tell if one or more of the fields are incorrect .
    - data quality requirements and define rules for measuring quality
    - create a strategy , outline a plan for your data quality , identify the data sets that meet your quality standart and the data sets thats need to be cleaned.
    - identify and correct errors in data. the method to error detection will depend on the database and data-set you are using
	
    	  