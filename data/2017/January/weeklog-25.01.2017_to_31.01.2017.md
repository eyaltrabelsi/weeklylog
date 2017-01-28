# weeklylog 25.01.2017 - 31.01.2017


## Articles
- [The Most Boring/Valuable Data Science Advice](https://databozo.posthaven.com/the-most-boring-slash-valuable-data-science-advice) `data science` `advice`
- [6 Differences Between Pandas And Spark DataFrames](https://medium.com/@chris_bour/6-differences-between-pandas-and-spark-dataframes-1380cec394d2#.mqx1a8xn6) `spark` `panda`
- [Data scientists mostly just do arithmetic and that’s a good thing](https://m.signalvnoise.com/data-scientists-mostly-just-do-arithmetic-and-that-s-a-good-thing-c6371885f7f6#.kmuqnqybs) `data science`
- [pandarize your spark dataframes](https://lab.getbase.com/pandarize-spark-dataframes/) `panda` `spark`
- [AWS Athena vs. Google BigQuery for interactive SQL Queries](http://www.slideshare.net/VadimSolovey/aws-athena-vs-google-bigquery-for-interactive-sql-queries) `aws athena` `big query` `vs`
- [Building Your Data Warehouse with Amazon Redshift](https://www.google.com/url?q=https://www.slideshare.net/mobile/AmazonWebServices/building-your-data-warehouse-with-amazon-redshift&source=gmail&ust=1481735670157000&usg=AFQjCNEUpv6y4oYhG6HUCcxbMgWVBhFkBg) `data warehouse` `data engineer` `redshift`
- [yelp redshift flow](https://news.ycombinator.com/item?id=12732356) `yelp` `redshift` 

## Videos
-[Artificial Intelligence at Facebook // Antoine Bordes, Facebook ](https://www.youtube.com/watch?v=OWvkpFZRaF4) `ai` `facebook` `ml`
-[23 Visualizations and When to Use Them](https://blog.dominodatalab.com/video-23-visualizations-use/) `favorite` `visualization`

## Packages
- [A formatter for Python files](https://github.com/google/yapf#id12) `python` `formatter`
- [Optionally drops any row with a missing value](https://github.com/rhiever/datacleaner/blob/master/README.md) `data science` `missing values` `python`
- [Prints descriptive statistics for all columns in a CSV file. Will intelligently determine the type of each column and then print analysis relevant to that type](http://csvkit.readthedocs.io/en/0.9.1/scripts/csvstat.html) `csv` `statistics` `cmd`
- [command line tool to convert json to csv] (http://github.com/jehiah/json2csv) `json` `csv` `cmd`

## Tools
- [Spotlight: Re:dash (redash.io)](https://thomas-barthelemy.github.io/2016/05/02/spotlight-redash/) `sql client` `visualization` `redshift` `mongodb` `mysql` `postgres`
- [aq - Query AWS resources with SQL](https://github.com/lebinh/aq) `aws` `query resources` 
- [A command-line fuzzy finder written in Go](https://github.com/junegunn/fzf) `fuzzy finder`

## Tips
- **Dimension reduction flow info**:    
    1) missing values:
       - if x>95 discard
         if 50=<x<=95 no imputation (missing value indicator)
         if x<50 imputation with indication
       - program:
         import pandas as pd
         desc =  df.describe().T
         desc[missing%] = 1 - (desc['count']/len(df))
    2) amount of variation- drop review variable that have very low variation (0)
    3) - PCA
         - dimensionality reduction technique which emphasizes variation
         - eliminates multi collinearity but excitability is compromised (uses orthogonal transfomation)
         - when to use
            - excessive multicolinearity
            - explanation of the predictors is not important
            - a slight overhead in implementation is ok
            - more suitable for unsupervised learning
       - Cluster analysis- 
         - dimensionality reduction technique which emphasizes correlation/similarity ( identify groups of variables that are correlated as possible among themself and as uncorrelated as possible with variables in other cluster)
         - reduce multi collinearity and explicitly is not always compromised
         - when to use (excessive multi collinearity ) or explanation of the predictors is important
       -  pairwise correlation 
          multi collinearity: when two or more variable are highly correlated with each other, droping one or more variables should help reduce dimensionality without substantial loss of information. (correlationn coefficient tolerence ~ 0.65)
          which to drop? use conditional index
    4) correlation with target, drop variables that have very low correlation with the target (meaning it wont be useful for the model)
    5) - forward selection:
           1. identify the best variables
           2. add the next best variables into the models
           3. and so on until some predefined criteria satisfied
       - LASSO, least absolute shrinkage and selection operation (selection+regularization
       - tree based method , forrest of trees to evaluate the importance of features
       - backward elimination:
           1. start with all variables included in the model
           2. drop the least useful variable
           3. and so on until some predefined criteria is satisfied
       - stepwise selection , similar to forward selection process but a variable can also be dropped if its deemed as not useful any more after a certain number of steps.
   