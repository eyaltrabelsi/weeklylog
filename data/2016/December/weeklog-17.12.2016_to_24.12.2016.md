# weeklylog 17.12.2016 - 24.12.2016

## Articles
- [Python Numpy Tutorial](cs231n.github.io/python-numpy-tutorial/) `numpy` `python` `101`
- [Summeray to linear algebra needed for machine learning practitioners](www.deeplearningbook.org/contents/linear_algebra.html) `linear algebra` `101` `favorite`
- [The myth of strong baseline](http://nlpers.blogspot.co.il/2014/11/the-myth-of-strong-baseline.html?m=1) `nlp` `ml` `baseline`
- [Why word2vec works](http://andyljones.tumblr.com/post/111299309808/why-word2vec-works) `word2vec` `intuition` `ml` `nlp` `favorite`
- [How big data is unfair](https://medium.com/@mrtz/how-big-data-is-unfair-9aa544d739de#.opmsnf7cz) `big data` `data engineer`
- [Linear Algebra for ml](http://www.deeplearningbook.org/contents/linear_algebra.html) `ml` `math` `linear algebra` `101` `math` `favorite` `data science`
- [Moving machine learning from practice to production](https://engineering.semantics3.com/2016/11/13/machine-learning-practice-to-production/) `ml` `data science` `favorite`
- [Bias in ML, and Teaching AI](http://nlpers.blogspot.co.il/2016/11/bias-in-ml-and-teaching-ai.html?m=1) `bias` `ml` `data science`
- [An Introduction to APIs (Application Programming Interfaces)](https://www.analyticsvidhya.com/blog/2016/11/an-introduction-to-apis-application-programming-interfaces-5-apis-a-data-scientist-must-know/?utm_source=feedburner&utm_medium=email&utm_campaign=Feed%3A+AnalyticsVidhya+%28Analytics+Vidhya%29) `api` `data engineer` `101`
- [It's ML, not magic: machine learning can be prejudiced](http://smerity.com/articles/2016/algorithms_can_be_prejudiced.html) `ml` `data science` 


## Videos
- [Deep Learning for NLP - Lecture 1](https://www.youtube.com/watch?v=AmG4jzmBZ88&feature=youtu.be) `deep learning` `neural networks` `nlp` `favorite`
- [Deep Learning for NLP - Lecture 2](https://www.youtube.com/watch?v=BCwBl_55n7s&feature=youtu.be) `nlp` `data engineer` `ml`
- [Candida Haynes | Architectures for Exploring Your Personal Data](https://www.youtube.com/watch?v=lpIOhgeRBbA&index=3&list=PLGVZCDnMOq0q9qZsHfueAJsMiCbtvlvWr) `data science`


## Snippets
- [allow to easily query salesforce resources using beatbox and retrieve a data frame] (https://gist.github.com/eyaltrabelsi/8a2a86e5509e8517880b6b935e6febf3)
- [bookmarklet which save time when opening a pull requests](https://gist.github.com/eyaltrabelsi/b988aef36db134d05c74f2d6c5ebb1d1)


## Principles
- DRY , Don’t repeat yourself , his is probably the single most fundamental tenet in programming is to avoid repetition. 
- KISS (Keep it simple, stupid!), Simplicity (and avoiding complexity) should always be a key goal. Simple code takes less time to write, has fewer bugs, and is easier to modify. 
- Avoid Creating a YAGNI (You aren’t going to need it)  You should try not to add functionality until you need it.
- Open/Closed Principle, Software entities. In other words, don't write classes that people can modify, write classes that people can extend.
- Write Code for the Maintainer, Almost any code that is worth writing is worth maintaining in the future, either by you or by someone else.
- Principle of least astonishment, The principle of least astonishment is usually referenced in regards to the user interface, but the same principle applies to written code. Code should surprise the reader as little as possible. 
- Single Responsibility Principle, A component of code should perform a single well defined task.
- Minimize Coupling- Any section of code (code block, function, class, etc) should minimize the dependencies on other areas of code. This is achieved by using shared variables as little as possible. 
- Hide Implementation Details - Hiding implementation details allows change to the implementation of a code component while minimally affecting any other modules that use that component.
- Law of Demeter, Code components should only communicate with their direct relations .
- Avoid Premature Optimization, Don’t even think about optimization unless your code is working, but slower than you want.
- Separation of Concerns , Different areas of functionality should be managed by distinct and minimally overlapping modules of code.
- Embrace Change, This is the subtitle of a book by Kent Beck, and is also considered a tenet of extreme programming and the agile methodology in general. Many other principles are based on the concept that you should expect and welcome change. In fact very old software engineering principles like minimizing coupling are related directly to the requirement of making code easier to change. Whether or not you are an extreme programming practitioner, this approach to writing code just makes sense. http://www.amazon.com/gp/product/0321278658
- Command–query separation (CQS), It states that every method should either be a command that performs an action, or a query that returns data to the caller, but not both. In other words, asking a question should not change the answer. 


## Tips
- **Pagination Techniques in different apis**:
    - sendgrid: every api calls return number of rows, for each source  there is a diffrent limit of rows for each call and than you update the offset. thus if a api call return less rows than the limit specified , it means it was the last page and you can stop.
    - salesforce: every api calls return 3 things fetched rows,indicator if fetched all rows, and if indicator is false than a "pointer" to the rest of the query.  thus if a api call return the indicator to false rows than we need to query salesforce with the query locator more.
    - chargify: every api calls return number of rows, for each source  there is a diffrent limit of rows for each call and than you update the page. thus if a api call return less rows than the limit specified , it means it was the last page and you can stop.
    - zendesk: every api calls return result which contain two improtant variables results which is fetched rows, and next_page which is the url for contienued query. if next_page doesnt exists in result than it means we fetched the entire resource.
    - marketo : every api calls return result which contain two improtant variables results which is fetched rows, and moreResult which is the url for contienued query. if moreResult doesnt exists in result than it means we fetched the entire resource.
- **data info**:
	- real data are on highly curved manifolds (example rotated image)
- **neural network info**
    - neural network = running several logistic regreesion in the same time
	- typical activation function
		* reftifier f(x) = max(0,x)
		* smooth approximation f(x) = ln(1+e^x)
	- which activation function to use
		* most papers use tanh, but for certain problems rectifier can be usefulll (espacialy for conv nets)
		* changing the ativation function has only minor effects
	- hidden layers rule of thumb:
		* number and sizes of the hidden layers can have large impact on performance
		* more hidden layers => more parameters to learn => more data needed
		* start with small number of hidden layers and increase the number of hidden layers stepwise until you find an optimum. 
		* typically decreasing sizes for the hidden layers for example 200dim => 100dim =>50 dim
	- neural netowork with one hidden layer is universal approximator, but not all functions can be represented efficiently with single hidden layer
- **intuition to method on neural network from human**:
	- how human generalize form few example:
		* they transfer knowledge from previous learning ( representation, explanatory factor)
		* previous learning from : unlabeled data + labels for other tasks
		* prior: shared underlying explanatory factors, in between p(x) and p(y|X)
	-  human first learn simpler concepts using generic learning  algorithm and then compose then to more comples ones)  inspired learning multiple levels of representation - exponential gain for some functions.

- **settings up development and tests set info**:   
    - choose dev and test set from distribution that reflect what data you expect to get in the future and want to do well on.
    - choose dev and test sets from the same distribution if possible
    - choose single number evaluation metric for your team to optimize.
      if there is multiple goals that you care about consider combining them into a single formula
    - machine learning is highly iterative process, you may try many dozen of ideas before finding one that you are satisfied with
    - having dev/tests set and single number evaluation metrics help you quickly evaluate algorithm and therefore iterate faster
    - when starting out on a brand new application, try to establish dev/test set and metric quickly (less than week)
    - the old heuristic of 70/30 train/test split does not apply for problems where you have a lot of data 
      the dev and tests set can be much less than 30 percents of the data
    - your dev set should be large enough to detect meaningful changes in the accuracy of your algorithm, your test set should be big enough to give you a confident estimate of a final performance of your system
    -  if ever your dev set and metric are no longer pointing your team in the right direction quickly change them.
        * if you had overfit the dev set , get more dev set data
        * if the actual distribution you care about is different from the dev/test set distribution, get new dev/test set data
        * if your metric is no longer measuring what is most important to you , change the metric. 
    
    
