# weeklylog 18.11.2016 - 25.11.2016

## Articles
- [Neural Networks, Types, and Functional Programming](http://colah.github.io/posts/2015-09-NN-Types-FP/) `neural network` `functional programming` 
- [Analyzing the Graph of Thrones](http://www.lyonwj.com/2016/06/26/graph-of-thrones-neo4j-social-network-analysis/) `data exploration` `neo4j` `data engineer` `favorite` 
- [Some empirically derived testing principles](http://www.drmaciver.com/2015/04/some-empirically-derived-testing-principles/) `testing` `best practices` 
- [Some things that might help you make better software](http://www.drmaciver.com/2016/10/some-things-that-might-help-you-write-better-software/) `best practices` 
- [UNDERSTANDING CONVOLUTIONAL NEURAL NETWORKS FOR NLP](http://www.wildml.com/2015/11/understanding-convolutional-neural-networks-for-nlp/) `convolutional neural networks` `neural networks` `favorite` `ml` `nlp` 
- [How To Setup A Learning Routine At Work](https://medium.com/xeneta/how-to-gain-new-skills-at-work-923bb088a352#.axo6c6z6h) `learning routine` 
- [Amazon Redshift Best Practices for Designing Queries](http://docs.aws.amazon.com/redshift/latest/dg/c_designing-queries-best-practices.html) `redshift` `data engineer` `best practices`  
- [Tutorial: Tuning Table Design](http://docs.aws.amazon.com/redshift/latest/dg/tutorial-tuning-tables.html) `redshift` `data engineer` `favorite` `table flow` 

## Packages
- [Automatic model code generator for SQLAlchemy](https://pypi.python.org/pypi/sqlacodegen) `ddl` `sqlalchemy` `python` `bash` `data engineer` 
- [A collection of various different notebook extensions for Jupyter](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) `ipython notebook` `jupyter notebook` `favorite` `data science` 
- [Simulacrum allow generate random DataFrame according to object definition](https://github.com/jbrambleDC/simulacrum) `test` `random` `pandas` `dataframe` `simulate` 
- [SNAKEVIZ](https://jiffyclub.github.io/snakeviz/) `snakeviz` `python` `profiling` `ipython notebook` 

## Videos
- [Uses and Best Practices for Amazon Redshift](https://www.youtube.com/watch?v=reQtXquDpzo) `redshift` `data engineer` `best practices` 
- [Build an Autoencoder in 5 Min - Fresh Machine Learning #5](https://www.youtube.com/watch?v=GWn7vD2Ud3M&list=PL2-dafEMk2A6Kc7pV6gHH-apBFxwFjKeY&index=5) `ml` `auto encoder` `101` `neural networks` 
- [Redshift Panel Discussion with AWS, Clever, Lumosity and Chartio](http://landing.chartio.com/aws-redshift-and-chartio-event-recording) `redshift` `data engineer` `best practices` `favorite` 
- [Data Structure -Binomial heap -Fibonacci heap](https://www.youtube.com/watch?v=rK41MvSeCMM) `data structures` `binomial heap` `theory`

## Tips
- in order to open finder in terminal the fbe written following command should  "open . trick"    
- Data Project tips:
    - An exploratory phase is needed to round up the available data and start the conversation accross the company.
    - The scope of the first deliverables should be expected to be narrow and incremental. Don’t let lose the momentum by shooting for too disruptive projects. Let a thousand flowers bloom.
    - Then, expand your goals well and focus on ROI. Prioritize.
- Testing tips:
    - 100% coverage is mandatory.
    - There is no substitute for hard work.
    - You need both very general and very specific tests.
    - All bugs result in tests.
- RDBMS tips:
    - Choosing which indexes to create requires the database designer to analyze a trade-off. In practice, this choice is one of the principal factors that influ­ ence whether a database design gives acceptable performance. Two important factors to consider are:
        * The existence of an index on an attribute may speed up greatly the exe­ cution of those queries in which a value, or range of values, is specified for that attribute, and may speed up joins involving that attribute as well.
        * On the other hand, every index built for one or more attributes of some relation makes insertions, deletions, and updates to that relation more complex and time-consuming.
    - But When modifications dominate, it is costly to have materialized views, or even indexes, on the data.
- Postgress tips
    - Use COPY to load all the rows in one command, instead of using a series of INSERT commands. The COPY command is optimized for loading large numbers of rows; it is less flexible than INSERT, but incurs significantly less overhead for large data loads. Since COPY is a single command, there is no need to disable autocommit if you use this method to populate a table.
- Redshift notes:
    - redshift keep meta data  of each slice of min , max value which can reduce the need for scan the entire slice.
