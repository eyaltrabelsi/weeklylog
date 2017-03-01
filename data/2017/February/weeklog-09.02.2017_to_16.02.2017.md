# weeklylog 09.02.2017 - 16.02.2017

## Articles
- [How to deal with Features having high cardinality](https://www.kaggle.com/forums/f/15/kaggle-forum/t/16927/how-to-deal-with-features-having-high-cardinality?forumMessageId=95887) `feature engineering` `data engineer` `high cardinality` `favorite`
- [Read a small random sample from a big CSV file into a Python data frame](https://gist.github.com/eyaltrabelsi/ebb8da1bad2b79cf732fccb432790780) `data exploration` `random sampling` `data engineer` `csv` `favorite`
- [My Standard Work for every new competition](https://www.kaggle.com/forums/f/15/kaggle-forum/t/19959/my-standard-work-for-every-new-competition) `kaggle` `flow` `ml` `data science`
- [Master the command line, in one page](https://github.com/jlevy/the-art-of-command-line) `favorite` `terminal`
- [Linux and Unix shuf command tutorial with examples](https://shapeshed.com/unix-shuf/) `favorite` `bash` `shuffling` `sampling` `shuf`
- [Using R for Customer Segmentation](https://ds4ci.files.wordpress.com/2013/09/user08_jimp_custseg_revnov08.pdf) `favorite` `customer segmentation`
- [28 Jupyter Notebook tips, tricks and shortcuts](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/) `favorite` `tips` `ipython notebook`
- [Timing and Profiling in IPython](http://pynash.org/2013/03/06/timing-and-profiling/) `profiling` `ipython notebook` `favorite`
- [Python & JSON: Working with large datasets using Pandas](https://www.dataquest.io/blog/python-json-tutorial/) `json` `large` `data exploration` `favorite`
- [MAKING PUBLICATION READY PYTHON NOTEBOOKS](http://blog.juliusschulz.de/blog/ultimate-ipython-notebook) `ipython notebook` `publication ready`
- [Data Science at the Command Line](http://datascienceatthecommandline.com/) `data science` `favorite` `command line` `tools`

## Videos
- [Fordham Career Workshop](https://www.youtube.com/watch?v=HqWVXom_PIw) `data science` `tips`
- [Deep Learning for NLP - Lecture 4 - Autoencoders](https://www.youtube.com/watch?v=FSKag11y8yI&feature=youtu.be) `deep learning` `neural networks` `autoencoders` `nlp` `ml`

## Packages
- [Magnificent app which corrects your previous console command](https://github.com/nvbn/thefuck) `cmd` `correct`
- [JSON -> Relational DB Column Types](https://github.com/wrobstory/malort) `json` `relational` `schema` 
- [Tools for diffing and merging of Jupyter notebooks](https://github.com/jupyter/nbdime)  `diffing` `merging` `jupyter notebook`
- [Interactive data exploration with Altair] (https://github.com/altair-viz/altair_widgets) `ipython notebook` `altair` `data exploration`
- [Python module that makes working with XML feel like you are working with JSON](https://github.com/martinblech/xmltodict) `json` `xml` `big` `python`
- [Missing data visualization module for Python](https://github.com/ResidentMario/missingno) `missing data` `data visualization` `python`

## Tips
- **Indication of messy data**:
    - there are some na values that pandas didnt recognize  
    - deduplicate
    - split by column
    - join column
    - flag mark condition
    - removing rows
    - normalization , min max normalization z score normalizer, decimal scaling normalization    
- **Diffrent methods to deal with outliers**:
    - unvariate method this method look for data points with extreme values on one variable
    - multivariate method here we look for unusale combination on all variables
    - minkowski error , this method reduces the contribution of potential outliers in the training process.    
- **Numeric transformation to deal with skew**:
    - cube root, x^(1/3) for right skewed data negative. not as effective at normalizing as log transform
    - reciprocal 1/x for making small values bigger and big value smaller. zero values and negative values	
    - square x^2 left skewed data.negative values
    - square root x^(1/2) right skewed data. negative values
    - log , ln(x) for right skew data , escpecially good at handling higher order powers of 10. zero, negative values
            