# weeklylog 01.11.2016 - 08.11.2016

## Articles
- [DATA SCIENCE AND THE PERFECT TEAM](http://101.datascience.community/2016/09/22/data-science-and-the-perfect-team/) `code` `data science` `communication` `statistic`
- [27 Jupyter Notebook tips, tricks and shortcuts](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/?utm_campaign=Data%2BElixir&utm_medium=email&utm_source=Data_Elixir_101) `ipython notebook` `tips` `tricks` `favorite`
- [Making data analytics work for you—instead of the other way around](http://www.mckinsey.com/business-functions/digital-mckinsey/our-insights/making-data-analytics-work-for-you-instead-of-the-other-way-around?utm_campaign=Data%2BElixir&utm_medium=email&utm_source=Data_Elixir_101) `analytics`
- [HOW TO STICK OUT FROM THE CROWD IN THE UBER ENGINEERING INTERVIEW PROCESS](https://eng.uber.com/recruit-q-a/) `favorite` `interview` `uber`
- [Say NO to Venn Diagrams When Explaining JOINs](https://blog.jooq.org/2016/07/05/say-no-to-venn-diagrams-when-explaining-joins/) `venn diagrams` `visualization` `joins` 
- [Why You Should Design Your Database to Optimise for Statistics](https://blog.jooq.org/2016/10/05/why-you-should-design-your-database-to-optimise-for-statistics/) `data engineer` `optimization` `statistics` `db`
- [Model evaluation, model selection, and algorithm selection in machine learning](http://sebastianraschka.com/blog/2016/model-evaluation-selection-part1.html) `model evaluation` `model selection` `ml`
- [Why Pylint is both useful and unusable, and how you can actually use it](https://codewithoutrules.com/2016/10/19/pylint/) `pylint` `favorite` `best practice` `tips`
- [Two-Way Tables and the Chi-Square Test](http://www.stat.yale.edu/Courses/1997-98/101/chisq.htm) `statistics` `chi-squre` `statistical tests` 

## Packages
- [A collection of various different notebook extensions for Jupyter](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) `ml` `ipython notebook` `jupyter notebook` `extentions` `favorite`
- [RISE: "Live" Reveal.js Jupyter/IPython Slideshow Extension](https://github.com/damianavila/RISE) `reveal.js` `magic` `ipython extention` `slideshow`
- [Pretty HTML/XML rendering with syntax highlighting for BeautifulSoup objects in IPython notebook and qtconsole.](https://github.com/Psycojoker/ipython-beautifulsoup) `beautifulsoup` `magic` `ipython extention` `html parsing` `html rendering`
- [D3 block magic for Jupyter notebook](https://github.com/ResidentMario/py_d3) `d3` `magic` `ipython extention` `visualization`
- [Drag’n’drop Pivot Tables and Charts for Jupyter/IPython Notebook, care of PivotTable.js](https://github.com/nicolaskruchten/jupyter_pivottablejs) `pivot` `visualization` `ipython notebook` `jupyter notebook` `data exploration`
- [IPython widgets for the Jupyter Notebook ](https://github.com/ipython/ipywidgets) `interactive` `input` `ipython notebook` `jupyter notebook` 
- [Defines a %%cache cell magic in the IPython notebook to cache results of long-lasting computations in a persistent pickle file](https://github.com/rossant/ipycache) `cache` `magic` `ipython notebook` `jupyter notebook` `performance`
 

## Tips
- **DWH tips**:
    - Natural keys created by operational source systems are subject to business rules outside the control of the DW/BI system. For instance, an employee number (natural key) may be changed if the employee resigns and then is rehired. When the data warehouse wants to have a single key for that employee, a new durable key must be created that is persistent and does not change in this situation.
    - date dimension: They reason that if the date key in the fact table is a date type column, then any SQL query can directly constrain on the fact table date key and use natural SQL date semantics to filter on month or year while avoiding a supposedly expensive join. 
    - Null-valued measurements behave gracefully in fact tables. The aggregate functions (SUM, COUNT, MIN, MAX, and AVG) all do the “right thing” with null facts.
    - The numeric measures in a fact table fall into three categories. The most flexible and useful facts are fully additive; additive measures can be summed across any of the dimensions associated with the fact table. Semi-additive measures can be summed across some dimensions, but not all;
    - In general, dimensional designers must resist the normalization urges caused by years of operational database designs and instead denormalize the many-to-one fixed depth
    - Fact tables that record financial transactions in multiple currencies should contain a pair of columns for every financial fact in the row. One column contains the fact expressed in the true currency of the transaction, and the other contains the same fact expressed in a single standard currency that
    - There are three basic fact table grains: transaction, periodic snapshot, and accu- mulcting snapshot. In isolated cases, it is useful to add a row e ective date, row expiration date, and current row indicator to the fact table,.
    - Declare a high-level commitment to a data quality culture.
        * Drive process reengineering at the executive level.
        * Spend money to improve the data entry environment.
        * Spend money to improve application integration.
        * Spend money to change how processes work.
        * Promote end-to-end team awareness.
        * Promote interdepartmental cooperation.
        * Publicly celebrate data quality excellence.
        * Continuously measure and improve data quality.
    - We have already remarked that each quality screen has to decide what happens when an error is thrown. The choices are: 1) halting the process; 2) sending the o ending record(s) to a suspense file for later processing; and 3) merely tagging the data and passing it through to the next step in the pipeline. The third choice is by far the best choice, whenever possible. Halting the process is obviously a pain because it requires manual intervention to diagnose the problem, restart or resume the job, or abort completely. Sending records to a suspense file is often a poor solu- tion because it is not clear when or if these records will be fixed and re-introduced to the pipeline
    - pitfalls:
        * Become overly enamored with technology and data rather than focusing on the business’s requirements and goals.
        * Fail to embrace or recruit an influential, accessible, and reasonable senior management visionary as the business sponsor of the DW/BI e ort.
        * Tackle a galactic multiyear project rather than pursuing more man- ageable, although still compelling, iterative development e orts.
        * Allocate energy to construct a normalized data structure, yet run out of budget before building a viable presentation area based on dimensional models.
        * Pay more attention to back room operational performance and ease- of-development than to front room query performance and ease of use.
        *  Make the supposedly queryable data in the presentation area overly complex. Database designers who prefer a more complex presentation should spend a year supporting business users; they’d develop a much better appre- ciation for the need to seek simpler solutions.
        * Populate dimensional models on a standalone basis without regard to a data architecture that ties them together using shared, conformed dimensions.
        * Load only summarized data into the presentation area’s dimensional structures.
        * Presume the business, its requirements and analytics, and the under- lying data and the supporting technology are static.
        * Neglect to acknowledge that DW/BI success is tied directly to busi- ness acceptance. If the users haven’t accepted the DW/BI system as a founda-
    - Develop Initial Index Plan understanding how the relational database’s query optimizer and indexes work, the database administrator also needs to be keenly aware that DW/BI requirements di er significantly from OLTP requirements. Because dimen- sion tables have a single column primary key, you’ll have a unique index on that key.

