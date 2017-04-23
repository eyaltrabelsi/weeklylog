# weeklylog 09.04.2017 - 16.04.2017

## Articles
- [6 areas of AI and machine learning to watch closely](https://medium.com/@NathanBenaich/6-areas-of-artificial-intelligence-to-watch-closely-673d590aa8aa#.w3j7frclx) `ml` `ai` `data science`
- [How Joins Work](https://periscopedata.com/blog//how-joins-work.html?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=revue) `joins` `sql` `data engineer`
- [Using Apache Spark 2.0 to Analyze the City of San Francisco's Open Data](https://www.youtube.com/watch?v=K14plpZgy_c) `spark2` `analysis` `big data` `data engineer`
- [Guide to Encoding Categorical Values in Python](http://pbpython.com/categorical-encoding.html) `categorical` `encoding` `data science` `favorite`
- [Semi join and Anti join](https://blog.jooq.org/2015/10/13/semi-join-and-anti-join-should-have-its-own-syntax-in-sql/) `sql` `data engineer` `anti join` `semi join` `favorite`
- [data exploration with python 2](http://blog.districtdatalabs.com/data-exploration-with-python-2) `data exploration` `python` `data engineer` `data scienece`
- [Kaggle Titanic Competition Part VI- Dimensionality Reduction](http://www.ultravioletanalytics.com/2014/11/26/kaggle-titanic-competition-part-vi-dimensionality-reduction/) `kaggle` `titanic` `ml` `data science` `dimensionality reduction` 
- [Kaggle Titanic Competition Part VII- Feature Importance](http://www.ultravioletanalytics.com/2014/12/01/kaggle-titanic-competition-part-vii-random-forests-and-feature-importance/) `kaggle` `titanic` `ml` `data science` `feature importance` 
- [Kaggle Titanic Competition Part VIII- Hyper-parameter Optimization](http://www.ultravioletanalytics.com/2014/12/03/kaggle-titanic-competition-part-viii-hyperparameter-optimization/) `kaggle` `titanic` `ml` `data science` `hyperparameter optimization`


## Packages
- [bridge between Scikit-Learn's machine learning methods and pandas](https://github.com/paulgb/sklearn-pandas/blob/master/README.rst) `python` `pandas` `ml` `scikit-learn`
- [A fast Python implementation of locality sensitive hashing](https://github.com/kayzhu/LSHash) `lsh` `similarity` `python`
- [Tabula is a tool for liberating data tables trapped inside PDF files](https://github.com/tabulapdf/tabula) `pdf` `python` `scraping` `tables`
- [Spark Magic for Jupyter](https://github.com/jupyter-incubator/sparkmagic) `ipyhton` `jupyter` `magic` `spark` 


## Videos
- [AWS Summit Tel Aviv 2016: Building Big Data Applications on AWS](https://www.youtube.com/watch?v=B6vtyXYsb-w&list=PLhr1KZpdzukfwJ-T-43QC8MLoE7gOJa6Y&app=desktop) `big data` `aws` `data engineer` `amazon` `favorite`  
- [AWS Summit Tel Aviv 2016: Gaining Operational Insights out of Your Logs](https://www.youtube.com/watch?v=YN1SxzPHdq4&list=PLhr1KZpdzukfwJ-T-43QC8MLoE7gOJa6Y&index=11) `insight` `logs` `aws` `amazon` `devops` 
- [016. Process Mining Data Science in Action](https://www.youtube.com/watch?v=kIeLaNzw9hI) `process mining` `data science` `data mining` `favorite` 


## Tips
- **ETL using EMR vs ELT using RDBMS**:
    - Cost Benefits
        * By moving ETL processing to Hadoop-based platform, we free up capacity (and potentially licensing costs) on the existing commerical RDBMS (Oracle) where the processing currently takes place
        * Costs are further reduced by the 'elastic' provisioning and cost model of the cloud service. You only pay for the size of the cluster necessary for your workload, for the duration that it took to execute.
        * In this instance we wanted to enrich the data, and proved Spark as an appropriate tool to do so. Running on Elastic Map Reduce we could provision this automagically, run our processing, and have the EMR cluster terminate itself once complete. The compute part of the equation is entirely isolated, and can be switched in and our of the architecture as required.
- **Summarization methods info**:
    - extractive summarization 
        - Problem 1: Bias with limit on summary size
        - Problem 2: Verbose
            ◦ May contain irrelevant information
            ◦ Not suited for smaller devices
    - abstractive summary
        - Problem: HARD
        - Some methods require manual effort 
        - Some methods rely on deep NL understanding 
            - Domain dependent
            - Impractical – high computational costs
    - Shallow abstractive summary 
        - General
            - Generates concise summaries using: existing text, inherent redundancies) 		
            - Uses minimal external knowledge
        - Code
            - Pre condition:
                - Set of sentences:
                    - Topic specific (ex. battery life of ipod)
                    - POS annotated
            - Step 1: Generate graph representation of sentences (Opinosis-Graph which naturaly capture:
                    - Naturally captures redundancies
                    - Captures gapped subsequences)
                    - Captures collapsible structures
            - Step 2: Find promising paths (candidate summaries) & score these candidates
            
