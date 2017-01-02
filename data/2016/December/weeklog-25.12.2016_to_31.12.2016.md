# weeklylog 17.12.2016 - 24.12.2016

## Articles
- [Deconvolution and Checkerboard Artifacts](http://distill.pub/2016/deconv-checkerboard/) `deconvolution` `vision` 
- [8 Reasons Why Analytics / Machine Learning Models Fail To Get Deployed](https://www.analyticsvidhya.com/blog/2016/05/8-reasons-analytics-machine-learning-models-fail-deployed/) `pitfalls` `models` `analytics`
- [From both sides now: the math of linear regression](http://katbailey.github.io/post/from-both-sides-now-the-math-of-linear-regression/) `statistics` `linear regression` 
- [Model evaluation, model selection, and algorithm selection in machine learning Part II - Bootstrapping and uncertainties](http://sebastianraschka.com/blog/2016/model-evaluation-selection-part2.html) `bootstrapping` `ml` `data science`
- [ 30-בדיקות-bi-ו-dwh-לעומת-הבדיקות-בתחומים-אחרים](http://www.dwh.co.il/blogs/entry/30-%D7%91%D7%93%D7%99%D7%A7%D7%95%D7%AA-bi-%D7%95-dwh-%D7%9C%D7%A2%D7%95%D7%9E%D7%AA-%D7%94%D7%91%D7%93%D7%99%D7%A7%D7%95%D7%AA-%D7%91%D7%AA%D7%97%D7%95%D7%9E%D7%99%D7%9D-%D7%90%D7%97%D7%A8%D7%99%D7%9D) `favorite` `bi` `tests` `data engineer`
- [Topic Models using words2vec](https://github.com/RaRe-Technologies/gensim/blob/develop/docs/notebooks/topic_methods.ipynb) `nlp` `ml` `topic models` `word2vec` `data science`
- [Machine Learning with Weak Supervision](http://hazyresearch.github.io/snorkel/blog/weak_supervision.html) `favorite` `ml` `weak supervision` `data science`
- [Improve your Dev and Ops skills with Troubleshooting Theory](https://blog.dnsimple.com/2016/11/troubleshooting-theory/) `devops` `troublshoting`
- [What are actionable insights?](https://shapescience.xyz/blog/what-are-actionable-insights/) `bi` `actionable` `insight`   
- [The shortcomings of data science](https://shapescience.xyz/blog/the-shortcomings-of-data-science/) `favorite` `data science` `ml` `models`
- [Up to date remote data access for pandas, works for multiple versions of pandas](https://pandas-datareader.readthedocs.io/en/latest/) `Yahoo! Finance` `Google Finance` `pandas` `data source`

## Videos
- [Max Tsvetovat | Beyond Sentiment Emotion Mining with Python and machine learning](https://www.youtube.com/watch?v=Fw8BnYMC5sY) `favorite` `sentiment analysis` `nlp` `ml` `data science`
- [Ajinkya More | Resampling techniques and other strategies](https://www.youtube.com/watch?v=-Z1PaqYKC1w) `resampling` `data science` 

## definition
- deep learning: neural network number of hidden layers is available .
   
## Principles
- in theory ,practice and theory are the same. in practice they are not
- the purpose of life is to be defeated by greater and greater things
- the best time to plant a tree is 25 years ago the second best time is today
- i have not failed i just found 10,000 ways that does work
- aerodynamically the bumblebee shouldnt be able to fly but it doesnt know so it goes on flying anyway
- confidence is the result of constant work and dedication

## Tips   
- **3 possible sources of uncertainty**:
	- inherent stochastic in the system being modeled. for example quantum mechanic.
	- incomplete observability. even deterministic systems can appear stochastic when we cannot observe all the variables that drive the behavior of the system.
	- incomplete modeling. when we use a model that must discard some of the information we have observed, the discarded information results in uncertainty in the model prediction
- **deep leanings motivation**:
	- ability to learn complex, highly varying functions with much greater variation than examples.
	- ability to learn with little human input the low level, intermediate,and high level abstractions that will be useful to represent  complex functions
	-  ability to learn from a very large set of examples, computation time for training should scale well with the number of examples
	- ability to learn from mostly unlabeled data
	- ability to exploit the synergies present across a large number of tasks aka multi task learning
	- strong unsupervised learning
- **neural networks info**:
    - feed forward networks
        * the most simple network architecture
        * info flow only in one direction
        * input layer represent my data
        * output layer represent possible labels
    - not dimensionality so much as number of variations
        * guassian kernal machine need least k example to learn a function that has 2k zero crossing along some line
        * guasiian kernal machine to learn some maximally varying function over d inputs require 2^d examples
    - initialization of wights and bias:
        * the bias is typically initialized to 0
        * the weights are randomly initialized (use glorot style uniform initialization)
- **neural networks tips**:
    - defining the error function in back propagation is an important aspect in designing a deep neural network
- **sparse and shared in deep architecture info**:
    - deep learning algorithm are based on learning intermediate representation which can be shared across tasks hench they can leverage unsupervised data and data from similar tasks
    - sharing components in deep architecture - polynomial expressed with shared components : advantage may group axoponantly because same neuron can be 'sliced'/'represented' in different way
    - multi task learning:  
	    * deep architecture learn good intermediate representation  that can be shared across tasks
        * good representation that disentangle underlying factors of variations make sense for many tasks concern subset of the factors*    
    - combining multiple sources of evidence with shared representation 
        * example event url person  and history words url
        * share representation of the same types across data sources,
        * shared learning representations help propagate information among data sources
    -  sparse representations :
        * just add penalty on learned representation
        * information disengaging 
        * more likely to be linearly separable (high dimensional space)
        * locally low dimensional representation = local chart
        * high dim sparse = efficient variable size representation = data structure
- **comparing against strong baseline pitfall**:
    - If we're going to ask the question about whether an evaluation strategy is "good" or "bad" we have to ask ourselves why are we doing this evaluation thing in the first place. 
      (A) I could have been trying to show that some new external source of knowledge is useful; 
      (B) I could have been trying to show that some new technique is useful.
      One problem is that "strong" isn't a total order. there are lots of ways to be better than such a baseline, and so "beating" it does not teach me anything. 
      If I want to show you that X is important, then I should show you an experiment that isolates X to the best of my ability and demonstrates an improvement, preferably also with an error analysis
- **BI testing info**:
    - quantity comparison between source to target
    - testing predicate , wrong business logic and filtering
    - validate keys
    - performance
    - In the erd validate there are no self joins
    - integration tests 
    - metadata validation 
    - naming conventions