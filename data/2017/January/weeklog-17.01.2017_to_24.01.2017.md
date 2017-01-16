# weeklylog 17.01.2017 - 24.01.2017


## Articles
- [The Theorem Every Data Scientist Should Know](http://www.jeannicholashould.com/the-theorem-every-data-scientist-should-know.html) `theorem` `big number theory` `probability` `data science`
- [Massive Internet Attack Floods the World with Fake Data](http://www.datasciencecentral.com/m/blogpost?id=6448529%3ABlogPost%3A493788) `fake data` 
- [Fits like a GloVe: “Betta” style with dense word vectors](https://gab41.lab41.org/street-style-guide-vector-transformations-betta-work-2ad8d9829587#.vqopkz283) `glove` `word vectors` `favorite` `ml` `data science`
- [The Most Boring/Valuable Data Science Advice](https://databozo.posthaven.com/the-most-boring-slash-valuable-data-science-advice) `data science` `advice`
- [6 Differences Between Pandas And Spark DataFrames](https://medium.com/@chris_bour/6-differences-between-pandas-and-spark-dataframes-1380cec394d2#.mqx1a8xn6) `spark` `panda`
- [Data scientists mostly just do arithmetic and that’s a good thing](https://m.signalvnoise.com/data-scientists-mostly-just-do-arithmetic-and-that-s-a-good-thing-c6371885f7f6#.kmuqnqybs) `data science`
- [AWS Athena vs. Google BigQuery for interactive SQL Queries](http://www.slideshare.net/VadimSolovey/aws-athena-vs-google-bigquery-for-interactive-sql-queries) `aws athena` `big query` `vs`
- [Building Your Data Warehouse with Amazon Redshift](https://www.google.com/url?q=https://www.slideshare.net/mobile/AmazonWebServices/building-your-data-warehouse-with-amazon-redshift&source=gmail&ust=1481735670157000&usg=AFQjCNEUpv6y4oYhG6HUCcxbMgWVBhFkBg) `data warehouse` `data engineer` `redshift`
- [yelp redshift flow](https://news.ycombinator.com/item?id=12732356) `yelp` `redshift` 

## Videos
- [ETL Is Dead, Long-live Streams](https://www.infoq.com/presentations/etl-streams) `data engineer` `etl` `streams` 

## Packages
- [Elizabeth is a library to generate dummy data. This library easy to use and very useful when you need to bootstrap a database](https://github.com/lk-geimfari/elizabeth) `dummy data` `python` 
- [Python module to perform under sampling and over sampling with various techniques](https://github.com/scikit-learn-contrib/imbalanced-learn) `sampling` `ml` `python` 
- [Superset is a data exploration platform designed to be visual, intuitive, and interactive](https://github.com/airbnb/superset) `airbnb` `data exploration` `visual` `data engineer` 
- [Let your Python tests travel through time](https://github.com/spulec/freezegun) `python` `tests` `time` 

## Tools
- [json incremental digger](https://github.com/simeji/jid) `json` `search` `bash` 
- [The Knowledge Repository (BETA)](https://github.com/airbnb/knowledge-repo/blob/master/README.md) `airbnb` `knowledge sharing` 

## Tips
- data visualisation categories info:	
	- deviation, emphasis variation from a fixed reference point. typically the reference point is zero but it can also be a target or along term average. can also be used to show sentiment.
		- spine chart , split a single value into 2 contrasting components (eg female/male)
		- diverging bar, a simple standard bar chart that can handle both negative and positive magnitude values
		- area chart the shared area of theses chart all otsa balance to be show
	- correlation, show the relationship between two or more variables. be mindful that unless you tell them otherwise many readeres will assume the relationship you show them to be casual
		- bubble , like a scatter-plot but add additional detail by sizing the circles according to a third variable and color to a fourth
		- animated bubble, like a scatter-plot but add additional detail by sizing the circles according to a third variable and color to a fourth and animation for a fifth
		- scatter-plot, the standard way to show the relationship between two continuous variables, each of which has its own axis
		- heat-map, a good way of showing the pattern between 2 categories of data, less good showing fine differences in amount
	- ranking, use where an item position in an ordered list is more important than its absolute or relative value. dont be afraid to highlight the points of interest.
		- slope graph, perfect for showing how ranks have changed over time or vary between categories.
	
	- distribution, show values in data-set and how often they occur. the shape (or skew) of a distribution can be a memorable way to highlighting the lack of uniformaty or equality in the data
		- box-plot, summarize (multiple distributions by showing the median and range of data)
		- histogram, the standard way to show a statistical distribution, keep the gaps between columns small to highlight the shape of the data
	
	- change, give emphasis to changing trends. these can be short (instraday) movements or extended series traversing decades or centuries. choosing the correct time period is important to provide suitable context for the reader
		- Area chart, use with chare these are good at showing 

	- composition, show how single entity can be broken down into its component elements if the reader intrest is soley in the size of the component. consider magnitude type charrt intead
		- waffle, good for showing % information they work best when used on whole numbers and work well in multiple layout form
		- stacked column , a simple way of showing part to whole relationship but can be difficult to read with more than a few componenets

	- spatial, used only when precise location or geographical pattern in the data are more important to the reader than anything else
		- heat-map , grid based data values mapped with intensive color scale. as choropleth map - but not snapped to an admin/political unit.
		- region hex, keep the overall shape and layout of geography so that its identifiable. yet lets you focus on the state or province level analysis
		- population tiles , a great way of showing how ares have different population size an





