# weeklylog 26.11.2016 - 30.11.2016

## Articles
- [Ten Ways Your Data Project is Going to Fail](http://www.martingoodson.com/ten-ways-your-data-project-is-going-to-fail/) `data project` `favorite` `pitfalls` 
- [Capturing semantic meanings using deep learning](https://www.oreilly.com/learning/capturing-semantic-meanings-using-deep-learning) `nlp` `ml` `word2vec` `deep learning` `favorite` `fasttext` `unsupervised learning`  
- [How is auto-encoder compared with other dimensionality reduction algorithms?](https://www.quora.com/How-is-autoencoder-compared-with-other-dimensionality-reduction-algorithms) `autoencoder` `ml` `unsupervised learning` `dimentionaly reduction` `pca` 
- [Stop Coding Machine Learning Algorithms From Scratch](http://machinelearningmastery.com/dont-implement-machine-learning-algorithms/) `ml` `tips` 
- [Deciding Whether to Reindex](http://docs.aws.amazon.com/redshift/latest/dg/r_vacuum-decide-whether-to-reindex.html) `redshift` `index` `data engineer` 
- [Understanding Convolutions](http://colah.github.io/posts/2014-07-Understanding-Convolutions/) `convolutions` `visualization` `ml` `favorite` `neural networks` 
- [Conv Nets: A Modular Perspective](http://colah.github.io/posts/2014-07-Conv-Nets-Modular/) `convolutions` `neural networks` `ml` 
- [6 Do’s and Don’ts for a Data Science Resume that Gets You Hired](http://www.galvanize.com/blog/6-dos-donts-data-science-resume-gets-hired/) `resume` `favorite` `data science` 
- [DeepMind and Blizzard to release StarCraft II as an AI research environment](https://deepmind.com/blog/deepmind-and-blizzard-release-starcraft-ii-ai-research-environment/) `deepmind` `blizzard` `ai research environment`

## Packages
- [Tutorial: automatic symmetrization using Gensim](https://github.com/RaRe-Technologies/gensim/blob/develop/docs/notebooks/summarization_tutorial.ipynb)
- [Utils for streaming large files (S3, HDFS, gzip, bz2...)](https://github.com/RaRe-Technologies/smart_open) `streaming` `context manager` `boto` `hdfs` `python`

## Videos
- [ARIES Overview, Types of Log Records, ARIES Helper Structures](https://www.youtube.com/watch?v=S9nctHdkggk) `restoration` `recovery` `aries` `data engineer` `rdbms` 
- [Using the OSEMN Process to Work Through a Data Problem](https://www.youtube.com/watch?v=w3LI1s7OBc4) `osemn` `data` `python` `data science` 
- [What to log, Physical, Logical, and Physiological Logging, Trade-Offs](https://www.youtube.com/watch?v=MR-89Lq5jCo&list=PLC4UZxBVGKteoQ2cO096j58IwjZrlki54&index=4) `log` `data engineer` `db` `data science`

## Snippets
- [query redshift from bash using psql](https://gist.github.com/eyaltrabelsi/b15ab470b22b0a89459c90385527a1e7)

## Tips
- **Redshift tips**:
    - to improve redshift's performance apply selective filters before join
    - timeout redshift during peak hours, since redshift's share the same computational resources
    - If a scheduled maintenance occurs while a query is running, the query is terminated and rolled back and you will need to restart it. Schedule long-running operations, such as large data loads or VACUUM operation, to avoid maintenance windows. You can also minimize the risk, and make restarts easier when they are needed, by performing data loads in smaller increments and managing the size of your VACUUM operations. For more information, see Load Data in Sequential Blocks and Vacuuming Tables.
    - If you use multiple concurrent COPY commands to load one table from multiple files, Amazon Redshift is forced to perform a serialized load, which is much slower and requires a VACUUM at the end if the table has a sort column defined. For more information about using COPY to load data in parallel, see Loading Data from Amazon S3.
    - If your data has a fixed retention period, we strongly recommend that you organize your data as a sequence of time-series tables, where each table is identical but contains data for different time ranges. 
      You can easily remove old data simply by executing a DROP TABLE on the corresponding tables, which is much faster than running a large scale DELETE, and also saves you from having to run a subsequent VACUUM to reclaim space. You can create a UNION ALL view to hide the fact that the data is stored in different tables. When you delete old data, simply refine your UNION ALL view to remove the dropped tables. Similarly, as you load new time periods into new tables, add the new tables to the view.
    - We strongly recommend that you individually compress your load files using gzip, lzop, or bzip2 when you have large datasets.
    - You can efficiently update and insert new data by loading your data into a staging table first. While Amazon Redshift does not support a single merge statement (update or insert, also known as an upsert) to insert and update data from a single data source, you can effectively perform a merge operation by loading your data into a staging table and then joining the staging table with your target table for an UPDATE statement and an INSERT statement. For instructions, see Updating and Inserting New Data.
    - Picking sort key If recent data is queried most frequently, specify the timestamp column as the leading column for the sort key.
      Queries will be more efficient because they can skip entire blocks that fall outside the time range.
      If you do frequent range filtering or equality filtering on one column, specify that column as the sort key.
      Amazon Redshift can skip reading entire blocks of data for that column because it keeps track of the minimum and maximum column values stored on each block and can skip blocks that don't apply to the predicate range.
      If you frequently join a table, specify the join column as both the sort key and the distribution key.
      This enables the query optimizer to choose a sort merge join instead of a slower hash join. Because the data is already sorted on the join key, the query optimizer can bypass the sort phase of the sort merge join
    - Picking dist key Distribute the fact table and one dimension table on their common columns. Your fact table can have only one distribution key.
      Any tables that join on another key will not be collocated with the fact table. Choose one dimension to collocate based on how frequently it is joined and the size of the joining rows.
      Designate both the dimension table's primary key and the fact table's corresponding foreign key as the DISTKEY. Choose the largest dimension based on the size of the filtered data set.
      Only the rows that are used in the join need to be distributed, so consider the size of the of the data set after filtering, not the size of the table.
      Choose a column with high cardinality in the filtered result set.
      If a dimension table cannot be collocated with the fact table or other important joining tables, you can improve query performance significantly by distributing the entire table to all of the nodes. Using ALL distribution multiplies storage space requirements and increases load times and maintenance operations, so you should weigh all factors before choosing ALL distribution.
    - In case only new values are getting update sometimes its better to split the table into old and new data and to vaccuum only thenew data
- **Data project pitfalls**:
    - Assume data in database is garbage unless its been used before
    - Data is not a commodity, it needs to be transformed into a product before it's valuable
    - You wont know the results are trash. selection bias, measurement bias, simpson paradox, etc for this you need scientists
    - For ETL hire data engineers for reporting hire bi analysts
    - Use an interpretable model first and then test against a baseline
    - the core of science is reproducibility please do , git , code review automated testing, data pipline etc
    - The real data will have weird outliers, or be boring. It will be too dynamic. It will be either too predictable or not predictable enough. Use live data from the beginning or your project will end in misery and self-hatred.
- **data science resume**:
    - DON’T: Bury your skills in fluff  
    - DON’T give up just because you don’t have on-the-job experience
    - DO: Emphasize metrics to showcase success
    - DO: Customize your resume for every employer
    - DO: Talk about data size
