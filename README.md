# name_ages
Predicting the age of Americans based on first names (as of the end of 2014).
**[View my IPython Notebook here](http://nbviewer.ipython.org/github/mdbecker/name_ages/blob/master/names_age.ipynb)**


## The technique
I'm pretty sure I originally heard about this technique a few years back at a data conference (either Strata or PyData).
I couldn't find the specific talk however I was able to find
[this paper](http://chenlab.ece.cornell.edu/people/Andy/Andy_files/1424CVPR08Gallagher.pdf) which mentions
similar techniques and [this article from fivethirtyeight](http://fivethirtyeight.com/features/how-to-tell-someones-age-when-all-you-know-is-her-name/)
which itself references [this blog article](http://cooldata.wordpress.com/2010/07/09/how-to-infer-age-when-all-you-have-is-a-name/).
Anyway, my point is, I didn't invent this idea, I just wanted to see if I could reproduce the results.

## The data
I decided to try the exact approach (and dataset) from the fivethirtyeight.

### Baby names
I grabbed the [baby name data from the Social Security Administration](http://www.ssa.gov/oact/babynames/names.zip)
which contains the first names of every baby born, "[with at least 5 occurrences](http://www.ssa.gov/oact/babynames/limits.html)," since 1880.

### Deaths
To properly predict how many people are alive **today** with any given name, we also need
[actuarial tables](http://www.ssa.gov/oact/NOTES/as120/LifeTables_Tbl_7.html) (more plesently referred to as
"Life Tables" by the SSA) to predict how many deaths have occured.

## The results
**[View my IPython Notebook here](http://nbviewer.ipython.org/github/mdbecker/name_ages/blob/master/names_age.ipynb)**

My results are almost exactly identical to the results from fivethirtyeight. I attribute the slight differences
I'm seeing in my results to the fact that I'm predicting out to January 1st, 2014 whereas fivethirtyeight
predicted out to January 1st, 2013. It's possible our techniques varied but I can't really tell since fivethirtyeight
does not show their work.

*Note that the order of the X axis is reversed in my graphs*
### Josephs
![fivethirtyeight](https://espnfivethirtyeight.files.wordpress.com/2014/05/silver-feature-joseph2.png?w=1150)
![me](https://raw.githubusercontent.com/mdbecker/name_ages/master/josephs.png)

### Brittanys
![fivethirtyeight](https://espnfivethirtyeight.files.wordpress.com/2014/05/silver-feature-brittany3.png?w=1150)
![me](https://raw.githubusercontent.com/mdbecker/name_ages/master/brittanys.png)
