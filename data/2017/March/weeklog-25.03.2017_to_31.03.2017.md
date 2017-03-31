# weeklylog 25.03.2017 - 31.03.2017

## Articles
- [Explaining Statistical Goodness of fit Tests with Beer (Statistics)](https://jasdumas.github.io/2017-01-04-choosing-a-stat-test-with-beer/) `statistics` `favorite` `chi-squared test` `t test` `anova test` `data science`
- [Developing machine learning strategy for business in 7 steps](https://www.altexsoft.com/blog/datascience/machine-learning-strategy-7-steps/?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=revue) `busyness strategy` `ml` `favorite` `data science`
- [A Practical Guide to Anonymizing Datasets with Python & Faker](http://blog.districtdatalabs.com/a-practical-guide-to-anonymizing-datasets-with-python-faker) `favorite` `data science` `data engineer` `anonymize` `python` `faker`
- [Asking the Right Questions of Your Data](http://www.slideshare.net/Hadoop_Summit/peterson-venugopal-june261120room211v2) `bi` `question asking` 
- [So You Call Yourself an Analyst? Part 1: Asking the Right Questions](https://moz.com/blog/so-you-call-yourself-an-analyst-part-1-asking-the-right-questions) `bi` `question asking` 
- [The Importance Of Outliers In Data](http://clearreturns.com/2013/06/27/the-importance-of-outliers-in-data/) `favorite` `data science` `data engineer` `outliers`
- [Crying analysis](http://www.robinwe.is/explorations/cry.html) `crying` `analysis`
- [More Data or Better Algorithms: The Sweet Spot](http://www.kdnuggets.com/2017/01/more-data-better-algorithms.html) `data science` `is it worth money`
- [Becoming a Data Scientist](http://www.pybloggers.com/becoming-a-data-scientist/) `data science` `how to`

## Videos
- [RISELab: Enabling Intelligent Real-Time Decisions](https://www.youtube.com/watch?v=XyEuhsmTF3U&index=4&list=PLTPXxbhUt-YVEyOqTmZ_X_tpzOlJLiU2k) `real time` `analytics`
- [Virtualizing Analytics with Apache Spark](https://www.youtube.com/watch?v=U3Jx21QNInc&index=5&list=PLTPXxbhUt-YVEyOqTmZ_X_tpzOlJLiU2k) `spark` `analytics` `data engineer`
- [Mitchell Hashimoto - Introducing Nomad and Otto](https://www.youtube.com/watch?v=aF_HPTHtqCA) `nomad` `devops`
- [GraphX: Graph Analytics in Spark- Ankur Dave (UC Berkeley)](https://www.youtube.com/watch?v=Y7hq5MudV9M) `graphx` `spark` `graphs` `big data` `data engineer`

## Packages
- [online natural language processing with word vectors](https://github.com/overlap-ai/words2map)  `word2vec` `visualization` `data science`
- [spark-redshift](https://github.com/databricks/spark-redshift) `spark` `redshift` `big data`
- [library which support most graph algorithms existed](https://github.com/igraph/python-igraph) `python` `graphs` `favorite`
- [Data Mining algorithms in python](https://github.com/bartdag/pymining) `data mining`

## Quates:
- "it really interesting how mother nature has her cool ways to hide her secrets"


## Tips:

- Publishing Data info:
    - Text
        * Avoid publishing text as Microsoft Word files. There are multiple incompatible versions of the format and they are read inconsistently outside Microsoft’s products.
        * Publishing text as PDF is okay. But remember that some of the purported benefits of PDF are myths: it is easily possible to edit any PDF file, so the files aren’t any more tamper-proof than any other format.
        * If your text is minimally styled, prefer a simple format. .txt files are the simplest format possible, and easy to read in any system.
    - Tables
        * Never publish tabular data as PDF. It’s nearly impossible to read this data with a computer, and so potential users need to do a lot of manual work to parse or re-type the data.
        * The most effective format for publishing table data is CSV. CSV stands for ‘Comma-separated values’, and is an option for Microsoft Excel’s exports.
    - Geographical Information
        * For small vector data, use GeoJSON or KML. These are simple, widely-adopted standards. Remember that these formats expect geographic coordinates in the WGS84 datum, which is easier to use for data consumers: so reproject before publishing. If you have high-accuracy projected data, provide a native-projection version for accuracy and a WGS84 version for ease of use.
        * For larger vector data, publish as Shapefiles.
        * A good, simple format for distributing raster data is GeoTIFF. It’s an open standard with many implementations. For larger raster datasets and non-geographical array data, NetCDF is another good choice with wide support.
        * Certain Esri data types like FileGDB and .zlas are intentionally encrypted and only supported by expensive Esri products, so they aren’t recommended for open data distribution. Likewise, GeoPDF is not recommended because it’s rarely implemented and also has legal restrictions.

- Data Flow info:
    - data -> store -> process -> store -> analyze -> answers
    - Acquire data
      * database
      * search
      * queue
      * stream storage
    - store to presistence
      * use hdfs for very requently accessed data
      * use s3 for frequently accesesd data
      * use s3 for infrequently accessed data
      * use amazon glacier for archiving cold data
                
- AWS tools and frameworks info:                                
    - machine learning
        * amazon ml
        * amazon emr(spark ml)
    - interactive
        * amazon redshift
        * amazon emr (presto, spark)
    - batch
        * amazon emr (hive, pig, spark, map reduce)
    - messaging
        * amazon sqs application on ec2
    - micro batch:
        * spark streaming
        * kcl
    - real time:
        * amazon kinessis
        * storm
        * aws lambda
        * kcl
        	                	        
- spark performance tips:
    - ensure enough partitions for concurrency
    - minimize memory consumption
    - minimize amount of data shuffled
    - know the standerded library
        	        