# weeklylog 01.03.2017 - 08.03.2017

## Articles
- [Data Exploration with Python, Part 1](http://blog.districtdatalabs.com/data-exploration-with-python-1?utm_campaign=Data%2BElixir&utm_medium=email&utm_source=Data_Elixir_112) `favorite` `data engineer` `python` `data science`
- [Practical Guide on Data Preprocessing in Python using Scikit Learn](https://www.analyticsvidhya.com/blog/2016/07/practical-guide-data-preprocessing-python-scikit-learn/) `favorite` `python` `data engineer` `scikit learn` `data science`
- [Which programming languages have the happiest (and angriest) commenters?](https://hackernoon.com/which-programming-languages-have-the-happiest-and-angriest-commenters-ebe91b3852ed#.euqa3yj4j) `programming` `analysis`
- [Cursors in Redshift](http://gcdatagroup.com/2016/07/24/cursors-in-redshift/) `data engineer` `redshift` `tableau`
- [How to ask good questions](https://jvns.ca/blog/good-questions/) `questions` `data science`
- [https://medium.com/pachyderm-data/jupyter-pachyderm-part-1-exploring-and-understanding-historical-analyses-2a37e56c6578#.8z785h397](Jupyter + Pachyderm — Part 1, Exploring and Understanding Historical Analyses) `data engineer` `pachyderm` `version` `data science`
- [How a Kalman filter works, in pictures](http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures/) `statistics` `kalman filters` `ml` `data science`
- [Stressed About Your Job Interview?](https://www.linkedin.com/pulse/stressed-your-job-interview-gagan-sarawgi?trk=prof-post) `job interview` `stress`
- [Approaching (Almost) Any Machine Learning Problem | Abhishek Thakur](http://blog.kaggle.com/2016/07/21/approaching-almost-any-machine-learning-problem-abhishek-thakur/) `favorite` `ml` `data science`
- [Steps for effective text data cleaning (with case study using Python)](https://www.analyticsvidhya.com/blog/2014/11/text-data-cleaning-steps-python/) `favorite` `text cleaning` `data engineer` `python` `data science`


## Videos
- [Fast Deep Learning at Your Fingertips](https://software.intel.com/en-us/videos/fast-deep-learning-at-your-fingertips) `data science` `intel` `ml` `deep learning` `neural networks`
- [The Race For AI: Practical Deep Learning- Exploring Embedded Spaces](https://www.youtube.com/watch?v=QtXPrJhfJqc) `ml` `data science` `embedded spaces` `neural network` `deep learning` `favorite`


## Packages
- [Bringing the python data stack to the shell prompt](https://github.com/robdmc/pandashells) `pandas` `shell` `analysis`
- [Data scraper for Facebook Pages, and also code accompanying the blog post How to Scrape Data From Facebook Page Posts for Statistical Analysis](https://github.com/minimaxir/facebook-page-post-scraper) `facebook` `scrape` `group` `page` `python`
- [Remove personally identifiable information from free text.](http://scrubadub.readthedocs.io/en/stable/index.html) `anonymize` `text` `data engineer`
- [A bash script utilizing git --date to commit in the past. Effectively hacking you back in time.](https://github.com/BillSkiCO/RX-Modulator) `hack` `git` `time travel`
- [Query AWS resources with SQL](https://github.com/lebinh/aq) `aws` `resources` `ec2` `sql`
- [A common, beautiful interface to tabular data, no matter the format](https://github.com/turicas/rows) `convert` `python` `csv` `json` 


## Tips
- **Statistical tests info**:              
    - Chi-squared tests compare observed frequencies to expected frequencies given independent normally distributed data.
      For example, is the distribution of beer style and production volume by year occur by random chance or is there a difference between beer style and how much is produced as a condition of year (either higher, lower, or the same form year to year)?
    - t-tests can be used to determine if two sets of data are significantly different from each other.
      For example, do brewery tour attendance differ on different weekend days - Do the amount of visitors on Saturday differ than on Sunday? let’s pose the question of interest by hypothesizing that there is no difference between attendance counts for Saturday or Sunday at the 0.05 significance level.
    - ANOVA, or Analysis of Variance tests the significance of group differences between two or more groups. This tests that there is a difference between groups but not which ones are different.
      For example, do beer ratings differ between age groups, 21-25, 26-30, 31+? As a hypothesis we can state that beer ratings will be no different among age groups - Beer drinkers of all ages give the same ratings for some beer that they are surveyed on.
- **Developing machine learning strategy for business steps**:              
    - Step 1. Articulate the problem
      There are generally two types of companies that engage in machine learning:
      * those that build applications with a trained ML model inside as their core business proposition 
      * those that apply ML to enhance existing business workflows. articulating the problem will be the initial challenge. 
      The bottom line here is to define the problem where standard business logic and the set of rules aren’t sufficient to solve it. Use machine learning when decisions heavily rely on a subjective opinion of an analyst or a decision maker.
    - Step 2. Consider the prescription
      What are you going to do with the insights you obtain? Can you automate the decision-making in this case?
      Coming up with prescriptions could be hard or it would involve a course of actions that can’t be automated at all.
      Moreover, insights that you will get may inspire the prescription measures that you could never think before unraveling hidden dependencies in your data.
    - Step 3. Ensure that the quality of your data is good enough
      * Qualify your data and decide the minimum prediction accuracy
      * Be ready to break down silos, anonymize, and share data
      * fix the Data
    - Step 4. Prepare to bridge the gap between technical and business vision
      any organizations have already recognized the need to introduce a chief analytics officer to their corporate frameworks. The person should have both business and tech expertise to lead the data science initiatives, envision the options to scale the machine learning application and reconcile business and technical vision.
      Otherwise, your data scientists should be ready to educate decision makers on the opportunities and limitations that different ML models present.
    - Step 5. Explore the options to hire the right talent
      the profession is extremely hyped,what makes data scientists so scarce and valuable is the blistering change in the technological landscape that outstrips educational capacities.
      Moreover, being a data scientist requires a rare skillset combination at the junction of math, statistics, programming, databases, and domain expertise.
      What are the options:
      * Hire a data scientist and be ready to engage
      * Homegrown specialists 
      * Find a vendor team
      * Build relationships with educational institutions
    - Step 6. Models become dated, be ready to iterate
      Most of the models are developed on a static subset of data, and they capture the conditions of the time frame when the data were collected. Once you have a model or a number of them deployed, they become dated over time and provide less accurate predictions. 
      There are two basic approaches to that:
      * Challenger testing. When the existing model is assumed to become less accurate, a new challenger model is introduced and tested against the deployed model.
        The old model is removed once the new one outperforms it. Then the process is repeated.
      * Online updates. The parameters of a model are changed under the continuous flow of new data.
    - Step 7. Decide whether you need a custom-built algorithm
      Building custom data models, their deployment, and further iterative development may be a serious financial and management burden for small and midsize businesses.
      Having an out-of-the-box algorithm doesn’t necessarily mean you won’t have to customize it to align with business objectives, but it might greatly reduce the financial difficulties.
