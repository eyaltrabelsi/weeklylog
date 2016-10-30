# weeklylog 26.10.2016 - 31.10.2016

## Articles
- [Communicating data science: A guide to presenting your work](http://blog.kaggle.com/2016/06/29/communicating-data-science-a-guide-to-presenting-your-work/?utm_content=buffer69f63&utm_medium=social&utm_source=facebook.com&utm_campaign=buffer) `communication` `data science`
- [Introduction to Data Visualization with Altair](http://pbpython.com/altair-intro.html) `favorite` `visualization` `101` `altair`
- [Why you don't want real-time analytics to be exact](http://blog.mikiobraun.de/2012/08/why-you-dont-want-real-time-analytics-to-be-exact.html) `data engineer` `exact` `vs` `real-time` `big data`
- [Why do Consulting skills matter in Data Science?](https://www.linkedin.com/pulse/20140917123625-41740903-the-importance-of-consulting-skills-in-data-science?trk=prof-post) `data science` `consulting skills` `soft skills`
- [A MAP OF THE PYDATA STACK](https://peadarcoyle.wordpress.com/2016/03/02/a-map-of-the-pydata-stack/) `python` `tools` `flow`
- [Data Science : Time To Change](https://medium.com/@chris_bour/data-science-time-to-change-8eac5ce81d1#.pnau9ii62) `data science` `process` `favorite` `flow`
- [More Google Big Data papers: Megastore and Spanner](http://blog.mikiobraun.de/2013/03/more-google-papers-megastore-spanner-voted-commits.html) `google` `megastore` `spanner` `data engineer`
- [WHY CODE REVIEW? OR WHY SHOULD I CARE AS A DATA SCIENTIST](https://peadarcoyle.wordpress.com/2016/09/19/why-code-review-or-why-should-i-care-as-a-data-scientist/) `code review` `best practices` `data science`
- [Tutorial: when Numpy isn't fast enough...](https://iamtrask.github.io/2014/11/23/cython-blas-fortran/) `ipyhon notebook` `cython` `fortran`


## Videos
- [Timothy Hopper | Sharing Your Side Projects Online and Making Your Github the Best Résumé It Ca](https://www.youtube.com/watch?v=uRul8QdYvqQ) `github` `mybinder` `resume`
- [PyTest, the testing framework you've been dreaming of by Eli Gur](https://www.youtube.com/watch?v=l0zjVKD7rx8&index=7&list=PL2ZIe_ro-J9p6s4n1EmKOhVo_Vs6Lnhc5) `pytest` `unit testing` `python`


## Tips
- By adding a semicolon at the end of a ipython notebook cell, the output is suppressed.
- airflow best practices: 
    - do you have longer running task? increase the hearbeat of the scedular to decrease load
    - smaller tasks make easier for debuggingg and retying 
    - properly choosoe your start date changing the sceuduale require change the dag id
    - backfills are userd to add runs where the schedular already went by
    - prefer many smaller dags over few large one (2.5 tasks per dag)
    - splitting dags as granulary as possible make it easier to turn defrent task groups on and off and easier reset
    - restart everything when deploying dag changes this is also something that improving the scedular also apear to need restarting when running with local executor
    - dont run command localty in the dag airflow ships with pythonop and bashopp they add flexibility butthis code run localy with no process isolationdag might demand a ton of packages 
    - Daily tasks run when the day is over
    - Not at the start of the day.

    
## Snippets
- [context manager to allow use git repository](https://gist.github.com/eyaltrabelsi/df31a13696b33188710a843e2ad657f4)


from users 

- [convert notebook to slideshow]() 
jupyter nbconvert <notebook-name> --to slides --post serve