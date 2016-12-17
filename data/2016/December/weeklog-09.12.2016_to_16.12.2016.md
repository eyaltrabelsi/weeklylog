# weeklylog 09.12.2016 - 16.12.2016

## Articles
- [Practical advice for analysis of large, complex data sets ](http://www.unofficialgoogledatascience.com/2016/10/practical-advice-for-analysis-of-large.html?utm_campaign=Data%2BElixir&utm_medium=email&utm_source=Data_Elixir_104&m=1)`data science` `google` `favorite` `data sets`
- [MySQL in the cloud at Airbnb](http://nerds.airbnb.com/mysql-in-the-cloud-at-airbnb/) `rds` `mysql` `data engineer` `favorite`
- [Redshift Performance & Cost](http://nerds.airbnb.com/redshift-performance-cost/) `data engineer` `redshift` `favorite`
- [So you want to manage technical debt?](https://medium.com/appaloosa-store-engineering/so-you-want-to-manage-technical-debt-7e5f376497f8#.jfap2codq) `technical debt`
- [Github Pull Request Bookmarklet](http://nerds.airbnb.com/github-pull-request-bookmarklet/) `github` `airbnb` `pull request` `bookmarklet`
- [Probabilistic Programming and Bayesian Methods for Hackers Chapter1_Introduction](http://nbviewer.jupyter.org/github/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/blob/master/Chapter1_Introduction/Ch1_Introduction_PyMC2.ipynb) `probability` `python` `favorite` `data science`
- [Differences between the L1-norm and the L2-norm (Least Absolute Deviations and Least Squares)](http://www.chioka.in/differences-between-the-l1-norm-and-the-l2-norm-least-absolute-deviations-and-least-squares/) `ml` `data science` `l1` `l2` `norm` `vs` 
- [Differences between L1 and L2 as Loss Function and Regularization](http://www.chioka.in/differences-between-l1-and-l2-as-loss-function-and-regularization/) `l1` `l2` `loss function` `vs` `ml` `data science`
- [Explain to Me: Generative Classifiers VS Discriminative Classifiers](http://www.chioka.in/explain-to-me-generative-classifiers-vs-discriminative-classifiers/) `generative classifier` `discriminative classifier` `ml` `data science` 
- [Stacking, Blending and Stacked Generalization](http://www.chioka.in/stacking-blending-and-stacked-generalization/) `blending` `stacking` `classifiers` `ml` `data science` 
- [Decoding The Thought Vector](http://gabgoh.github.io/ThoughtVectors/) `tought vector` `favorite` `ml` `data science` 
- [Which is Better : Boosting or Bagging](http://www.chioka.in/which-is-better-boosting-or-bagging/) `boosting` `bagging` `vs` `ml` `data science`

## Snippets
- [bookmarklet which save time when opening a pull requests](https://gist.github.com/eyaltrabelsi/b988aef36db134d05c74f2d6c5ebb1d1)
- [Disadvantages & Advantages Of incremental data load](https://gist.github.com/eyaltrabelsi/00fc8ebe48773e796717c2ec0eac3f99)

## Definitions
- The Philosophy of Bayesian Inference , You are a skilled programmer, but bugs still slip into your code. After a particularly difficult implementation of an algorithm, you decide to test your code on a trivial example. It passes. You test the code on a harder problem. It passes once again. And it passes the next, even more difficult, test too! You are starting to believe that there may be no bugs in this code...

## Principles
- rubber duck debugging: is a method of debugging code, where a programmer would carry around a rubber duck and debug their code by forcing themselves to explain it, line-by-line, to the duck.
  
## Tips
- **probability info**:
    - Paradoxically, big data's predictive analytic problems are actually solved by relatively simple algorithms [2][4]. Thus we can argue that big data's prediction difficulty does not lie in the algorithm used, but instead on the computational difficulties of storage and execution on big data.
      The much more difficult analytic problems involve medium data and, especially troublesome, really small data. Using a similar argument as Gelman's above, if big data problems are big enough to be readily solved, then we should be more interested in the not-quite-big enough datasets.
- **Redshift info**:
    - Avoid using select *. Include only the columns you specifically need.
    - Use a CASE Expression to perform complex aggregations instead of selecting from the same table multiple times.
    - Don’t use cross-joins unless absolutely necessary. These joins without a join condition result in the Cartesian product of two tables.
      Cross-joins are typically executed as nested-loop joins, which are the slowest of the possible join types.
    - Use predicates to restrict the dataset as much as possible.
    - If possible, use a WHERE clause based on the primary sort column of the largest table in the query to restrict the dataset. 
      The query planner can then use row order to help determine which records match the criteria, so it can skip scanning large numbers of disk blocks.
      Without this, the query execution engine must scan the entire table.
    - Add predicates to filter tables that participate in joins, even if the predicates apply the same filters.
      The query returns the same result set, but Amazon Redshift is able to filter the join tables before the scan step and can then efficiently skip scanning blocks from those tables.
    - Avoid using functions in query predicates. Using them can drive up the cost of the query by requiring large numbers of rows to resolve the intermediate steps of the query.
    - In the predicate, use the least expensive operators that you can. Comparison Condition operators are preferable to LIKE operators. LIKE operators are still preferable to SIMILAR TO or POSIX Operators.
- **RDBMS info**:
    - there are several factors that make the index-based search more efficient than it seems.
        * The number of index blocks is usually small compared with the number of data blocks.
        * Since keys are sorted, we can use binary search to find K . If there are n blocks of the index, we only look at log2n of them.
    - The conclusion we draw is that any two actions of different transactions may be swapped unless:
        * They involve the same database element, and
        * At least one is a write.
    - The index may be small enough to be kept permanently in main memory buffers. If so, the search for key K involves only main-memory accesses, and there are no expensive disk I/O’s to be performed.
    - the secondary index is distinguished from the primary index in that a secondary index does not determine the placement of records in the data file. Rather, the secondary index tells us the current locations of records; that location may have been decided by a primary index on some other field. An important consequence of the distinction between primary and secondary indexes is that:
        * Secondary indexes are always dense. It makes no sense to talk of a sparse, secondary index. Since the secondary index does not influence location, we could not use it to predict the location of any record whose key was not mentioned in the index file explicitly.
