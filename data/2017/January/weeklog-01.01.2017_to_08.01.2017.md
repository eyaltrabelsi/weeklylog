# weeklylog 01.01.2017 - 08.01.2017

## Articles
- [Must-Have Metrics for Outbound](https://blog.chartio.com/blog/must-have-metrics-for-outbound) `outbound` `metrics` 
- [Sales Metrics: Why You Should Care](https://blog.chartio.com/blog/sales-metrics-what-works-and-what-doesnt) `sales` `metrics` 
- [Using a Staging Table for Efficient MySQL Data Warehouse Ingestion](http://mysql.rjweb.org/doc.php/staging_table#flip_flop_staging) `tip` `data warehouse` `data engineer`
- [Documenting Your Data Warehouse](https://blog.chartio.com/blog/documenting-your-data-warehouse) `favorite` `documentation` `data warehouse` `bi` `data engineer` 
- [Probability and InformationTheory](http://www.deeplearningbook.org/contents/prob.html) `favorite` `information theory` `probability` `ml` `data science`
- [Image Augmentation for Deep Learning With Keras](http://machinelearningmastery.com/image-augmentation-deep-learning-keras/) `data augmentation` `keras` `deep learning` `neural networks` `favorite` `ml` `data science` `image processing`
- [DATA + DESIGN book](https://infoactive.co/data-design/) `ml` `visualization` `favorite` `data science` `data engineer` 
- [Python for Computational Science and Engineering book](http://www.southampton.ac.uk/~fangohr/teaching/python/book.html) `computational science` `linear algebra` `python` `calculus` `probability` `data engineer`
- [ETL vs ELT: The Difference is in the How](http://panoply.io/blog/etl-vs-elt-the-difference-is-in-the-how/) `etl` `elt` `vs` `data engineer`
- [Using Docker in PyCharm](https://blog.jetbrains.com/pycharm/2015/12/using-docker-in-pycharm/) `docker` `pycharm` `favorite` 
 
## Videos
- [Ten SQL Tricks that You Didn’t Think Were Possible (Lukas Eder)](https://www.youtube.com/watch?v=mgipNdAgQ3o) `tip` `favorite` `sql` `data engineer`
- [Tips & Tricks on Tuning Slow running SQLs in PostgreSQL](https://www.youtube.com/watch?v=SnrkMYbrS3E) `sql` `tip` `data engineer`
- [Vishal Patel | A Practical Guide to Dimensionality Reduction Techniques](https://www.youtube.com/watch?v=ioXKxulmwVQ&index=23&list=PLGVZCDnMOq0qLoYpkeySVtfdbQg1A_GiB) `favorite` `dimentional reduction` `ml` `data science`

## Packages
- [a python library for parsing unstructured western names into name components](https://github.com/datamade/probablepeople) `python` `name components` `feature engineering`
- [PyPrind - Python Progress Indicator Utility](https://github.com/rasbt/pyprind)`python` `process bar`
- [SQL profiling and introspection for applications using sqlalchemy](https://github.com/inconshreveable/sqltap) `python` `sql` `profiling` `sqlalchemy` `data engineer`
- [python implementation of the parquet columnar file format](https://github.com/dask/fastparquet) `python` `parquet` `data engineer`
- [Feather: fast, interoperable binary data frame storage for Python, R, and more powered by Apache Arrow](https://github.com/wesm/feather) `arrow` `storage` `python` `data engineer`
  
## Tips
- **the general approch for extracting text ml**:
	- extract sentences that contain specific attribute
	- pos tag and extract unigrams/bigram/trigram centered on nouns
	- extract features: words around nouns, bad of words, word vectors, position of noun, length of sentence
	- map training data to create a balance positive and negative training set
- **semi supervision info**:
    - For many tasks, we can leverage various heuristics and existing datasets as weak supervision. We can express these various signals in one unifying framework: as functions which label data.
- **sampling methods info**:
    - random under-sampling:
        * algo: randomly under-sample example from L
        * disadvantage: may lose informative examples    
    - tomek link removal:
        * definition: a pair of example is called tomek link if they belong to diffrent classes and are each other nearest neighbout. 
        * what: remove all tomek links from dataset
        * variant: remove tomek link members from L	   
    - nearmiss-1:
        * what: retain points from L whose mean distance to the k nearest points in S is lowest
- **data dimensions info**:
	- Completeness, Are critical data values missing? A database with missing data values is not unusual, but when the information missing is critical, then completeness is an issue. 
	  If a customer’s first name and last name are mandatory but the job title is optional, a record can be considered complete even if a job title is not available.
	  Is your data missing values?
	- Conformity, Is the data following standard data definitions? 
	  For example, are dates in a standard format? Maintaining conformity to standard formats are important to maintaining consistent structure and nomenclature for sharing and internal data management.
	- Accuracy , Is the data accurate to the “real-world” values expected? Incorrect spellings, misplaced decimals, untimely or out of date data can lead to inaccurate analysis.
	  If the sales from a customer are not the true sales or the email address of a contact is misspelled, the data is not accurate.
	  Are your data values correct?
	- Timeliness, Is the data available when expected and needed? Timeliness depends on the user’s expectations and needs.
	  If tracking information is delayed or a customer’s purchasing information is not updated in real-time then the timeliness could be an issue.
	- Consistency ,Does the data across several systems reflect the same information? If data is reported across multiple systems, it should have the same information.
	  If one database reports a customer’s account as active, while another reports the account as closed, the data set is not consistent.
	- Integrity Is the data valid across the relationships and can all the data in a database be traced and connected? For example, in a customer database there should be a valid customer/sales relationship.
	  If there are sales data without a customer then that data is not valid and is an orphaned record. The inability to link related records may introduce duplication across your systems.
- **feature engineering info**:
    - if all features have been obfuscated its impossible to construct new features by their meaning , a three new features can be mean vluae standar deviantion and count of non zero value of each instanch
    - feature engineering can greatly improve prediction accuracy
    - another lesson i can take away from this competition is that cross validation help significantly 
    - very common approach to creating new features is to combine numeric features with mathematical operations , common one are x+y xy x^2 logx
- **Reviews Corpuses info**:
    - sentiment140:
	    * 1.6 million labeled english tweets
	    * with :) etcs hold positive negative
	    * idely regarded as a somewhat noisy data set due to this choice of labeling criterion
    - amazon reviews snap corpus
	    * 34 k amazon of various products and start from 1 to 5	sometimes researchers collapse to jus positive and negatics
    - samples from the twitter garden hose:
        * 470m tweets collected over 4 month this
        * not  all tweets are suitable for traditional tasks (ascii art etc)	
- **word2vec info**:
    - the general logic behind word2vec is " you shall know a word by the company it keeps"
