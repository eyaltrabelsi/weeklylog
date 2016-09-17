# weeklylogs 28.08.2016 - 31.08.2016

## Articles
- [Markov Chains Explained Visually](http://setosa.io/ev/markov-chains/) `data visualization` `markov chain`
- [Eigenvectors and Eigenvalues Explained Visually](http://setosa.io/ev/eigenvectors-and-eigenvalues/) `favorite` `data visualization` `eigen vector` `eigen value`
- [Solving unicode Problems](https://www.azavea.com/blog/2014/03/24/solving-unicode-problems-in-python-2-7/) `python` `decode` `encode`
- [AWS: היכרות עם SxS - "השירותים הפשוטים" של אמזון - חלק א'](http://www.softwarearchiblog.com/2015/04/aws-simple-services-part1.html?m=0) `sqs` `sns` `aws`
- [GTA is teaching self-driving cars how to navigate better in the real world](http://thenextweb.com/artificial-intelligence/2016/09/12/gta-teaching-self-driving-cars-steer/) `gta` `self driving cars` `gta` `games`
- [Run periodic jobs in PostgreSQL](https://www.citusdata.com/blog/2016/09/09/pgcron-run-periodic-jobs-in-postgres/) `postgres` `cron` `maintenance`
- [Conditional probability Explained Visually](http://setosa.io/ev/conditional-probability/) `data visualization` `conditional probability`
- [The Myth of RAM](http://www.ilikebigbits.com/blog/2014/4/21/the-myth-of-ram-part-i), [2](http://www.ilikebigbits.com/blog/2014/4/28/the-myth-of-ram-part-ii), [3](http://www.ilikebigbits.com/blog/2014/4/29/the-myth-of-ram-part-iii) `favorite` `ram` `big o`
- [How to Choose a Data Format](http://www.svds.com/how-to-choose-a-data-format/) `favorite` `data format`
- [Database Best Practices](http://www.svds.com/how-to-choose-a-data-format/), [2](http://soa-java.blogspot.com/2013/01/database-guidelines-rdbmssql.html?m=1) `favorite` `best practices` `database` `bi` `tips` `rdbms`
- [How to beat the CAP theorem](http://nathanmarz.com/blog/how-to-beat-the-cap-theorem.html) `favorite` `cap theorem` `database` `architecture` `big data` `cassandra` `storm` `elephant db` 


## Videos
- [Pragmatic Unicode, or, How do I stop the pain?](https://www.youtube.com/watch?v=sgHbC6udIqc) `python` `decode` `encode`


## Snippets
- One can count file in folder by aws s3 ls --recursive s3://BUCKET_NAME/FOLDER_NAME | wc -l `s3` `snippet` `file count`
    
## Tips
- Boto performance:
    - instead of using s3.get_bucket(bucket_name) one can use s3.get_bucket(bucket_name, validate=False)

- Data Format:
    - fast write no space concern: just store your data in text format with the understanding that query times for large data sets will be longer
    - handle evolving data in your system: rely on Avro to save schemas. Keep in mind, though, that when writing files to the system Avro requires an pre-populated schema, which might involve some additional processing at the beginning.
    - optimized  analysis:  then you might want to take a look at a columnar format such as Parquet or ORC because they offer the best performance in queries, particularly for partial searches where you are only reading specific columns. However, the speed advantage might decrease if you are reading all the columns.
        
- RDBMS Tips:
    - How to choose which columns for index:
        * The primary and foreign keys columns are candidates for index.
        * Choose columns which not frequently updated, since index will degrade performance of DML  (update, insert, delete) operations (due to index table maintenance).
        * Choose columns which are used in order by / group by clauses since indexes will order the data to make these statements faster.
        * If you use range in where clause (e.g. between) use this range columns when making clustered index.
        * Use high selective / high cardinality columns.
        * Order is matter when creating composite indexes:  create highly selective indexes by using the most restrictive columns first.
        
    - When to use views:
        * Consider to use views in these cases:
        * To limit columns/tables that a user can see due to security/privacy concerns. You might restrict the view query to read only and limit the rows return.
        * To hide complex join, to represent a combination of tables.
        * To give meaningful names.
        * To absorb changes. When the data model in database changes, the application can still use the same query if we modify the view definition.
      note: VIEWs are your friends. They can be used to isolate database changes from the application, reducing the need for maintenance if the database changes.
      
    - Schema related:
        * Normalization is useful to avoid redundancy, consistency problem/update anomaly, deletion & insertion anomalies. So first try to normalize at least to the 3rd normal form. 
        * Reduce the size of table, you might use vertical partitioning or  horizontal partitioning . 
        * Make sure data/params types are correct (e.g. localization format, null usage)
        * Avoid too high abstract object since it's difficult to understand and can result in too many self-join.
        * Natural key vs artificial key (e.g. surrogate key/GUID): First prefer to use the natural key since it's more  meaningful and to avoid duplications (reuse existing column). But there are cases when you need an artificial key: when the natural key is not unique (e.g. names) or if you need to change the value.
        * Minimize the use of null for example by enforcing null constraint to force the application only sending no null values. You can also enforce default values (e.g. with DDL).
        * Each table must has primary key.
        * Provide documentation, describe all tables & relationships, DDL. The application programmers should be able to find documentations about any triggers, constraints & store procedures in your database.
        * don't use Reserved Word Overlap
        * Transportable Dates
        
    - Performance & Scalability
        * Use fewer resource (e.g. don’t use select *, reduce tables involved in join operation).
        * Use index. Make sure your queries do index seek instead of table scan or index scan. Clustered index is faster than non-clustered one.
        * Minimize table, columns, rows. 
        * Incremental update / paging big results.
        * Vertical partitioning: create smaller table which can be retrieve faster, e.g. split the 10 columns to a 4-columns table for frequency used, and the rest in a 6-columns table which need to be join for less frequency operations.
        * Avoid too much normalization. Denormalization to reduce joins
        * For better SELECT performance, index your JOIN columns.

    - Others
        * To version a database, a person can make SQL scripts and store them under VersionControl 
        


