# weeklylog 17.04.2017 - 24.04.2017

## Articles
- [64 vs 34 bit](https://www.infoq.com/news/2016/01/VS-64-bit) `hardware` `vs` 
- [Applications of PageRank to Recommendation Systems](https://web.stanford.edu/class/msande233/handouts/lecture8.pdf) `page rank` `data science` `data engineering` `favorite` `recommendation systems`
- [Optimizing Spark SQL JOIN statements for High Performance](https://intelligentinsight.wordpress.com/2016/07/05/optimizing-spark-sql-join-statements-for-high-performance/) `spark` `data engineer` `big data` `performance tuning`
- [Wavelet image hash in Python](https://fullstackml.com/2016/07/02/wavelet-image-hash-in-python/) `image` `hash` `similarity` `data enrichment`
- [Simple open Data tips](http://simpleopendata.com/) `data` `tips` `data science` `big data`  `favorite`  `data engineering`
- [Boosting Sales With Machine Learning](https://medium.com/xeneta/boosting-sales-with-machine-learning-fbcf2e618be3#.42f181exg) `sales` `ml` `nlp` `data science`
- [Advancing Research on Video Understanding with the YouTube-BoundingBoxes Dataset](https://research.googleblog.com/2017/02/advancing-research-on-video.html?m=1) `favorite` `dataset` `video` `favorite` `data science` `ml`
- [Clustering Similar Stories Using LDA](http://engineering.flipboard.com/2017/02/storyclustering) `clustering` `lda` `data science` `ml` `nlp` `favorite`
- [The Quartz guide to bad data](https://github.com/Quartz/bad-data-guide/blob/master/README.md) `data cleaning` `data validation` `data science` `data engineering` `favorite`
- [Working with Apache Spark: Or, How I Learned to Stop Worrying and Love the Shuffle](http://blog.cloudera.com/blog/2015/05/working-with-apache-spark-or-how-i-learned-to-stop-worrying-and-love-the-shuffle/) `spark` `big data` `shuffle`


## Videos
- [Large scale network analysis w/ python and igraph](https://www.youtube.com/watch?v=419yNuE4Jn0) `graphs` `igraph` `favorite`
- [Zeppelin Build and Tutorial Notebook](https://www.youtube.com/watch?v=CfhYFqNyjGc) `big data` `zepplin` `data engineering` 
- [Insights Without Tradeoffs: Using Structured Streaming in Apache Spark](https://www.youtube.com/watch?v=IJmFTXvUZgY&index=2&list=PLTPXxbhUt-YVEyOqTmZ_X_tpzOlJLiU2k) `favorite` `streaming` `spark` `structured streaming` `data engineering` `real tim`
- [Using Apache Spark for Intelligent Services](https://www.youtube.com/watch?v=B6w7tZKk_c8&list=PLTPXxbhUt-YVEyOqTmZ_X_tpzOlJLiU2k) `spark` `big data` `ml` `salesforce`


## Packages
- [A fast and friendly PDF scraping library](https://github.com/jcushman/pdfquery) `pdf` `python` `scraping`
- [A Python Perceptual Image Hashing Module](https://github.com/JohannesBuchner/imagehash) `image` `similarity` `hash` `python` 
- [Visual analysis and diagnostic tools to facilitate machine learning model selection](https://github.com/DistrictDataLabs/yellowbrick)
- [Comprehensive country code information, including ISO 3166 codes](https://github.com/datasets/country-codes)

## Definitions
- business process is essentially any function of the business which performs regularly that take and input make changes to it and provide output

## Tips
- **architectural data principles**:
      - decoupled data bus 
        * data -> store process -> store
      - use the right tool for the job
        * latency , throughput, access patterns
      - apply lambda architecture ideas
        * immutable (append only) log , batch / speed
      - leverage AWS managed services
        * no/low admin
      - be cost conscious
        * big data != big cost
- **Redshift vs spark**:
    -  Redshift has proved to be useful for interactive analysis of the data, but the processing of the data that would typically get done within an RDBMS (with associated license costs) can instead be done on technology such as Spark.
- **Thirteen causes of enterprise data quality problems**:
	- INITIAL DATA CONVERSION
		Databases rarely begin their life empty. More often, the starting poin
		n their lifecycle is a data conversion from some previously existing data source. And by a cruel twist of fate, it is usually a rather violent beginning. Data conversion usually takes the better half of new system implementation effort and almost never goes smoothly.
	- SYSTEM CONSOLIDATIONS
		Database consolidations are the most common occurrence in the information technology landscape. They take place regularly when old systems are phased out or combined.
	- MANUAL DATA ENTRY
		Despite high automation, much data is (and will always be!) typed into the databases by people through various forms and interfaces.
	- BATCH FEEDS
		Batch feeds are large, regular data exchange interfaces between sys- tems. The ever more numerous data- bases in the corporate universe communicate through complex spider webs of batch feeds.	
	- REAL-TIME INTERFACES
		More and more data is exchanged between the systems through real- time (or near real-time) interfaces.
	- DATA PROCESSING
		Data processing is at the heart of all operational systems.
	- DATA CLEANSING
		New methodologies have arrived that use automated data cleansing rules to make corrections en masse. These methods are 
		great value and I, myself, am an ardent promoter of the rule-driven 
		approach to automated data cleans- ing. Unfortunately, the risks and com- plexities of automated data cleansing are rarely well understood
	- DATA PURGING
		Old data is routinely purged from systems to make way for more data. This is normal when a retention limit is satisfied and old data no longer necessary. However, data purging is highly risky for data quality.
	- CHANGES NOT CAPTURED
		Data can become obsolete (and thus incorrect) simply because the object it describes has changed. 
	- PROCESS AUTOMATION	
		With the progress of information technology, more and more tasks are automated. 


    