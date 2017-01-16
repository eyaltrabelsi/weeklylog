# weeklylog 09.01.2017 - 16.01.2017

## Articles
- [Work remotely with PyCharm, TensorFlow and SSH](https://medium.com/@erikhallstrm/work-remotely-with-pycharm-tensorflow-and-ssh-c60564be862d#.ixfgut53a) `remote` `pycharm` 
- [ML Experiments at Sift Science, Part 1: Minimizing Bias](https://engineering.siftscience.com/ml-experiments-part-1-minimizing-bias/)`bias``ml` `data science`
- [The law of Large Numbers fails in big data](http://gtdatamining.blogspot.co.il/2016/09/the-law-of-large-numbers-fails-in-big.html) `big data` `law of large numbers` `data engineer`
- [The Power of Data Augmentation](https://deeplearningmania.quora.com/The-Power-of-Data-Augmentation-2) `image processing` `data augmentation` `ml` `data science`
- [Deep Learning Sentiment One Character at a T-i-m-e](https://gab41.lab41.org/deep-learning-sentiment-one-character-at-a-t-i-m-e-6cd96e4f780d#.c6n5ncbi2) `deep learning` `sentiment analysis` `ml` `data science` 
- [Feature engineering is just easier](https://gab41.lab41.org/feature-engineering-is-just-easier-1928d935ed17#.4r9zdphvk) `feature engineering` `ml` `data science` 
- [Can Word Vectors Help Predict Whether Your Chinese Tweet Gets Censored?](https://gab41.lab41.org/can-word-vectors-help-predict-whether-your-chinese-tweet-gets-censored-711e7682d12f#.g0mwz7cxl) `word vectors` `censorship` `favorite` `ml` `data science`
- [A Tour of Sentiment Analysis Techniques: Getting a Baseline for Sunny Side Up](https://gab41.lab41.org/a-tour-of-sentiment-analysis-techniques-getting-a-baseline-for-sunny-side-up-45730ec03330#.huhswgm09) `sentiment analysis` `101` `ml` `data science` 
- [Laying the Foundation for a Data Team](https://monzo.com/blog/2016/11/30/laying-the-foundation-for-a-data-team/?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=revue) `data team` `data science`
- [Machine Learning Basics](http://www.deeplearningbook.org/contents/ml.html) `favorite` `ml` `data science` 

## Videos
- [Advancing the Python Data Stack with Apache Arrow](https://www.youtube.com/watch?v=O8FwMyjezGk) `apache arrow` `python` `data engineering`
- [Pydata Paris 2016 - How Apache Arrow and Parquet boost cross-language interop](https://www.youtube.com/watch?v=ZGIIsK3-aJY) `apache arrow` `python` `data engineering`

## Tools
- [A proofreader for your data http://dataproofer.org/](https://github.com/dataproofer/Dataproofer) `csv` `data validation` `data engineer`
- [Producing your own git repository animated visualization video](https://www.ekreative.com/blog/producing-your-own-git-repository-visualization)`vizualizaion` `git`
- [Amazon Athena](https://aws.amazon.com/athena/?utm_source=hackernewsletter&utm_medium=email&utm_term=featured) `athena` `s3` `data engineer`
- [q - Run SQL directly on CSV or TSV files](https://github.com/harelba/q) `sql` `csv`

## Snippets
- [allow you to see which column has what type in dataframe](https://gist.github.com/eyaltrabelsi/441896ac5ffa49daa5614a3f57fa5f3c)


## Tips
- **Generative Classifiers VS Discriminative Classifiers info**:
	- Generative Classifiers, A generative classifier tries to learn the model that generates the data behind the scenes by **estimating the assumptions and distributions of the model. It then uses this to predict unseen data, because it assumes the model that was learned captures the real model. As we will see, this is often not true. An example is the Naive Bayes Classifier.
	- Discriminative Classifiers, A discriminative classifier tries to model by just depending on the observed data. It makes fewer assumptions on the distributions but depends heavily on the quality of the data (Is it representative? Are there a lot of data?). An example is the Logistic Regression.
	- when to use what:
		* The generative model does indeed have a higher asymptotic error (as the number of training examples become large) than the discriminative model but,
		* The generative model may also approach its asymptotic error much faster than the discriminative model – possibly with a number of training examples that is only logarithmic, rather than linear, in the number of parameters
-  **Boosting vs  Bagging info**:
	- Bagging is to have multiple classifiers trained on different under-sampled subsets and allow these classifiers to vote on a final decision, contrasting with just using one classifier.
	- Boosting is to have a series of classifiers to train on the dataset, but gradually putting more emphasis on training examples that the previous classifiers have failed (i.e. harder for classifiers to get it right), in the hope of that the next classifier will focus on these harder examples. So in the end, you will have a series of classifiers who are in general balanced but slightly more focused on the hard training examples.
	- when to use what :
		* In practice, boosting beats bagging in general, but either bagging and boosting will beat a plain classifier.
- **Conductive bias free experiment info**:
    - External data sources need to be versioned.
    We leverage a number of third-party data sources in our system, such as IP-Geo mappings and open proxy lists. 
    When running offline experiments, we need to ensure we only ever use the latest version of these data sources available at the point in time at which we are extracting features for a user:
    - Verify all new data sources are not biased in any way by ground truth. 
    In addition to ensuring external and derived data sources do not leak backwards in time, we also need to make sure the collection of these data sources is not a function of the labels we have collected. 
    For example, when backfilling some new data source from historical data, we can’t bias the backfill process towards more aggressively backfilling data for users belonging to the positive (i.e. fraudulent) class. 
    We have run into this exact issue in the past when experimenting with third-party social data sources, which led to some too-good-to-be-true initial results. 
    Since then, we have learned to more thoroughly vet all new data sources introduced into our pipeline, including the more recent introduction of an email age feature which is derived from our customers’ data.
    - To summarize, conducting representative and bias-free offline experiments can be challenging, and special attention needs to be paid to:
        * Train-test set creation, to ensure models are trained towards the proper objective.
        * Preventing cheating, to ensure evaluation of experiments is directionally correct.
        * Maintaining parity with the live system, to ensure experiment results more closely correlate to live results.
        * Experiment evaluation, to ensure experiments properly measure value to customers.
- **least square regression vs least absolute deviation regression info**:
    - least squares regression:
        * not very robust
        * stable solution
        * always one solution
        * no feature selection
        * non sparse output
        * computational efficient due to having analytical solutions
    - least absolute deviations regression:        
        * robust
        * unstable solution
        * possible multiple  solutions
        * built in feature selection
        * sparse output
        * computational inefficient due to having analytical solutions
