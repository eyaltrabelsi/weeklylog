# weeklylog 01.04.2017 - 08.04.2017

## Articles
- [segment tutorial](http://email.segment.com/e/c/eyJlbWFpbF9pZCI6Ik5UTTJPVGs2RndHN3NnSmtBQUp6QUJhTlZSb0JWakdENDVvVkNSaFlrTkNnQVcwNk5EUTJOemM1QUE9PSIsInBvc2l0aW9uIjowLCJocmVmIjoiaHR0cDovL2dyb3cuc2VnbWVudC5jb20vZGF0YS10cmFja2luZy1lc3NlbnRpYWxzLnBkZiIsImxpbmtfaWQiOjMyNTY5MTA1fQ/8ae9af51b68de98d56b0210a52fc15724b49d726aa6f02c015c3cb6f1604142f) `segment` `event system` 
- [Kaggle Titanic Competition Part I – Intro](http://www.ultravioletanalytics.com/2014/10/30/kaggle-titanic-competition-part-i-intro/) `kaggle` `titanic` `ml` `data science`
- [Kaggle Titanic Competition Part II – Missing Values](http://www.ultravioletanalytics.com/2014/11/03/kaggle-titanic-competition-part-ii-missing-values/) `kaggle` `titanic` `ml` `data science` `missing values`
- [Kaggle Titanic Competition Part III – Variable Transformations](http://www.ultravioletanalytics.com/2014/11/05/kaggle-titanic-competition-part-iii-variable-transformations/) `kaggle` `titanic` `ml` `data science` `variable transformation`
- [A guide to improving data integrity](https://www.oreilly.com/ideas/a-guide-to-improving-data-integrity?imm_mid=0eceb8&cmp=em-data-na-na-newsltr_20170201)
- [Open source guide](https://opensource.guide/) `open source` `favorite`
- [Treatment of Outliers](http://livebook.datascienceheroes.com/data_preparation/outliers_treatment.html) `outlier` `data science` `data engineer`
- [Intro to NLP with spaCy](https://nicschrading.com/project/Intro-to-NLP-with-spaCy/) `data science` `machine learning` `nlp` `spacy`
- [A Review of "Designing Data-Intensive Applications"](http://tech.marksblogg.com/designing-data-intensive-applications-review.html) `data engineering` 
- [ETL Offload with Spark and Amazon EMR - Part 3 - Running pySpark on EMR](https://www.rittmanmead.com/blog/2016/12/etl-offload-with-spark-and-amazon-emr-part-3-running-pyspark-on-emr/) `pyspark` `emr` `data engineering` `big data` `favorite`


## Videos
- [Scala Tutorial: Case Classes Explained](https://www.youtube.com/watch?v=ZLRt5MxJLIg) `scala` `101` `case classes`
- [Sparkling Pandas - using Apache Spark to scale Pandas](https://www.youtube.com/watch?v=AcyI_V8FeIU) `big data` `pandas` `spark` `big data`  `data engineering` 
- [Why Scala? ...by a hilarious Indian guy](https://www.youtube.com/watch?v=LH75sJAR0hc) `scala` `favorite`
- [Visualizing twitter discussions with networkx](https://www.youtube.com/watch?v=rGRuhVKd3D4) `graphs` `visualization` `networkx`


## Packages
- [unsupervised machine learning: Extract Article's Text in HTml documents](https://github.com/rodricios/eatiht) `python` `scraping` `html` 
- [pprofile + matplotlib = Python program profiled as an awesome heatmap!](https://github.com/csurfer/pyheat) `python` `profiling` `visualization`
- [Rapid Automatic Keyword Extraction algorithm using NLTK](https://github.com/csurfer/rake-nltk) `python` `keyword extraction` `nlp` `ml`


## Tips
- **types of processes info**:
    - batch should be processed within minutes or hours on cold data
        * daily/weekly/monthly reports
    - interactive should be processed within second on warm/cold data
        * self service dashboards
    - messaging should be processed within  milliseconds or seconds on hot  data
        * message event buffering
    - streaming should be processed within miliseconds or seconds on hot data
        * billing fraud alerts	

- **messages & stream storage**:
    - amazon sqs managed message queue service
    - apache kafka high throughput distibuted messaging system
    - amazon kinesis streams managed stream storage+ processing
    - amazon kinesiss firehose managed data delivery
    - amazon dynamo db managed nosql tables can be stream enabled		

- **Database optimizers**:
    - cardinality estimates are the most important ingrediant for dinding a good query plan.

- **fault tollerance info**
    - Since every data is replicated on x number of disks. probability of disk dying doesnt depend on the size of the cluster, so as the cluster go bigger the chances of permanently losting all three replicas is getting higher.
