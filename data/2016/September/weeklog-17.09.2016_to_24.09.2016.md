# weeklylogs 17.09.2016 - 24.09.2016

## Articles
- [MPython + Elasticsearch, First steps](https://tryolabs.com/blog/2015/02/17/python-elasticsearch-first-steps/),[2](https://github.com/ernestorx/es-swapi-test/blob/master/ES%20notebook.ipynb) `elastic search` `python` `101` `favorite`
- [Principal Component Analysis Explained Visually](http://setosa.io/ev/principal-component-analysis/) `data visualization` `pca`
- [כיצד מגדירים ארכיטקטורה? צעד אחר צעד](http://www.softwarearchiblog.com/2014/11/architecutre-definition-illustrated.html?m=0) `architecture` `chess` `oop`
- [Central Limit Theorem Visualized in D3](http://blog.vctr.me/posts/central-limit-theorem.html) `data visualization` `probability` `statistics` `central limit theorem`
- [Amazon Virtual Private Cloud] (http://www.softwarearchiblog.com/2016/06/aws-virtual-private-cloud.html?m=0) `devops` `aws` `routing` `vpc`
- [ארכיטקטורות ללא שרת (Serverless Architectures) - מה זה השטויות האלה?!](http://www.softwarearchiblog.com/2016/07/serverless-architectures.html?m=0) `serverless` `bass` `fass`
- [What is an intuitive explanation of overfitting?](https://www.quora.com/What-is-an-intuitive-explanation-of-overfitting?srid=zG&share=1#!n=60) `overfitting` `intuition` 
- [Entropy Explained, With Sheep] (https://aatishb.github.io/entropy/) `entropy` `favorite` `data visualization` `intuition`
- [Doing well in your courses] (http://cs.stanford.edu/people/karpathy/advice.html) `studying` `favorite` `tips`
- [Learning from Imbalanced Classes](http://www.svds.com/learning-imbalanced-classes/) `favorite` `ml` `classification` `imbalanced classes`


## Installation
- [ELK Stack on Mac OS X Yosemite](http://www.websightdesigns.com/wiki/ELK_Stack_on_Mac_OS_X_Yosemite) `mac` `elastic search` `logstash` `kibana` 
- [Chrome extension for full text history search!](https://github.com/lengstrom/falcon) `chrome extention` `text search` `browsing history`


## Videos
- [IPython Notebook best practices for data science](https://www.youtube.com/watch?v=JI1HWUAyJHE) `data science` `ipython notebook` `tips` 


## Tips
- How to squash all git commits into one? git rebase --root -i. For each commit except the first, change pick to squash
- Ipython Notebook tips:
    - html -> IFrame()
    - output x cell -> _x
    - save always .py and .html as well
    - naming notebook -> <date>-<developer>-<2-4 words desc>
    - [sql plugin] (https://github.com/catherinedevlin/ipython-sql)
    - [An Interactive Grid for Sorting and Filtering DataFrames in IPython Notebook](https://github.com/quantopian/qgrid)
    - [other great ipython extentions]()https://github.com/ipython/ipython/wiki/Extensions-Index
- Balancing Imbalanced Classes:
    - Oversampling and undersampling:
        - By oversampling The problem is that the separating lines we learn will have high bias 
        - We can do better by down-sampling the majority class to match that of the minority class. The problem is that the separating lines we learn will have high variability
        - one can  use bagging to combine these classifiers by
             1. take bootstrap samples from the original population 
             2. balance each sample by downsampling 
             3. learn decision tree from each
             4. majority vote   
    - Neighbor-based approaches
        - Tomek links are pairs of instances of opposite classes who are their own nearest neighbors. In other words, they are pairs of opposing instances that are very close together.
    - Synthesizing new examples: SMOTE and descendants
    - Adjusting class weights:
        - the minority class gains in importance (its errors are considered more costly than those of the other class) and the separating hyperplane is adjusted to reduce the loss.


## Packages
- [Python Elasticsearch Client](https://elasticsearch-py.readthedocs.io/en/master/) `data` `data engineer` `db` `client`
- [Better directory iterator and faster os.walk()](https://github.com/benhoyt/scandir) `python` `directory iterator`
- [Ipython notebook sql plugin] (https://github.com/catherinedevlin/ipython-sql) `sql` `ipython notebook` `extension`
- [An Interactive Grid for Sorting and Filtering DataFrames in IPython Notebook](https://github.com/quantopian/qgrid) `extension` `ipython notebook`
- [other great ipython extentions](https://github.com/ipython/ipython/wiki/Extensions-Index) `extension` `ipython notebook` `favorite`
