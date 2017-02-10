# weeklylog 01.02.2017 - 08.02.2017

## Articles
- [PEP 380 -- Syntax for Delegating to a Subgenerator](https://www.python.org/dev/peps/pep-0380/) `pep` `python`
- [Streaming Messages from Kafka into Redshift in near Real-Time](https://engineeringblog.yelp.com/2016/10/redshift-connector.html) `data engineer` `yelp` `kafka` `redshift` `streaming`
- [How the heck does async/await work in Python 3.5?](http://www.snarky.ca/how-the-heck-does-async-await-work-in-python-3-5) `favorite` `python` `python 3.5 features`
- [What kind of problems (if any) would there be combining asyncio with multiprocessing?](http://stackoverflow.com/questions/21159103/what-kind-of-problems-if-any-would-there-be-combining-asyncio-with-multiproces) `stackoverflow` `question` `asyncio` `python`
- [Streaming MySQL tables in real-time to Kafka](https://engineeringblog.yelp.com/2016/08/streaming-mysql-tables-in-real-time-to-kafka.html) `data engineer` `yelp` `kafka` `mysql` `streaming`
- [The three eras of business data processing](http://snowplowanalytics.com/blog/2014/01/20/the-three-eras-of-business-data-processing/) `etl` `data engineer`
- [A Brief History of the SMACK Stack](https://chiefscientist.org/a-brief-history-of-the-smack-stack-f382547e91fe#.ttmfmqi70) `smack` `spark` `101` `akka` `cassandra` `moses` `kafka`
- [More Than Just a Schema Store](https://engineeringblog.yelp.com/2016/08/more-than-just-a-schema-store.html)`data engineer` `yelp`
- [Detect and exclude outliers in Pandas dataframe](http://stackoverflow.com/questions/23199796/detect-and-exclude-outliers-in-pandas-dataframe) `pandas` `outliers` `favorite` `data exploration` `data science` `data engineer`

## Videos
- [CS 224D Lecture 2 - Lectures from 2015 deep learning](https://www.youtube.com/watch?v=T8tQZChniMk) `deep learning` `data science` `ml` `neural networks`

## Packages
- [Neo4j + vis.js = neovis.js. Graph visualizations in the browser with data from Neo4j](https://github.com/johnymontana/neovis.js) `neo4j` `visualization` `data exploration`
- [Iterative JSON parser with a standard Python iterator interface](https://pypi.python.org/pypi/ijson/)`data exploration` `data science` `data engineering`
- [A suite of utilities for converting to and working with CSV, the king of tabular file formats](https://github.com/wireservice/csvkit) `csvkit` `utils` `csv` 
- [YAML for command line](https://github.com/0k/shyaml) `data exploration` `data science` `data engineering` ``
- [A hacky debugger UI for hackers](https://github.com/snare/voltron) `debugger`

## Tips
- **Customer segmentation info**:
    - Recency
        * How long ago was last purchase? (days)
        * Measured for “As Of Date” of data set
        LastPurchaseDate
    - Frequency
        * How many orders in analysis period (2 ½ years)
        * Attempting to measure engagement
        NumberOrders
    - Monetary
        * What is total $ value of all orders in analysis period	
        TotalAmount
    - Breadth
        * How many different SKUs purchased?
        NumberSKUs
    - Tenure
        * How long as customer been with us?
        FirstPurchaseDate: interesting for tenure metric 
    – AsOfDate <- max(LastPurchaseDate)    
- **analysis folder format info**:
    - keep all your analyses under a folder name research 
    - each analysis should be in separate file with name and date
- **deal with Features having high cardinality info**:
    - For non-linear algorithms like RF you can also replace a categorical variable by the number of times it appears in the train set. This turns it into a single feature.
    - apply the "hashing trick"
    - If the high cardinality feature is not too high, often replace the categorical variable with the AVERAGE of the target variable (over records with the same feature) and sometimes add a VARIANCE (or standard deviation) column that can help mitigate low predictive power or low cardinality values in the feature. You could probably come up with other suitable functions depending on the data; 
      basically converting the single feature into a mini-model and recycling the output.
      One thing I do is try to ensure that the cardinality of the categorical information in the training set resembles that in the test/validation sets. That is, if I have a feature with values {A,A,A,B,C,C,D} in train, but test only has {A,B,B}, then eliminating the C and D records, and undersampling the A or oversampling the B records may resist overfitting.
- **kaggle contest info**:
    1. I use every new contest to update any general python environments (all Anaconda) I have on the 5 computers I may actually do coding on. (Even though this is not strictly necessary since I set up project environments, it's a trigger to keep things up to date.)
    2. Add the competition end date to my electronic and wall calendars.
    3. Update the kaggle evaluation metric wiki to reference back to the contest page.
    4. Identify any related contests
    5. Subscribe to the Forum
    6. Create a github repo, a standard folder structure, and a wiki so that I have a single place for model notes and to capture forum posts of interest. (I have a sub checklist for the steps, e.g., what I add to the .gitignore, etc.)
    7. Download the data
    8. Create virtual environments (conda) for my 3 linux machines with a standard set of libraries. Again, this is a separate sub checklist, and includes updating xgboost, theano, etc. Once I start a project, I do not update libraries unless absolutely necessary.
    9. Explore the data, which includes basic outlier analysis.
    10. Force myself to write error analysis code before I start building a model. (This is hard to stay true to, but worth the effort.)
    11. Start feature transformation, and finally model building	

