# final-project

##### Comments from Dr. J (5/6/2020): 

* Your graphs look great!  I love the graphs showing the rates by state and with the political leanings colored.  
* For gender and poverty status, I can see why you're not sure these are the best plots; they are a little bit overwhelming.  I wonder if it would make more sense to do an overall plot of poor vs. not poor rather than by state, and the same with gender, since most states seem to follow the trend that females have higher rates than males and that poor have higher rates than non-poor, however it looks like you don't have rates for the US overall in your dataset.  So you would have to combine them by adding up the number of F and M and dividing by adding up the sample sizes.  I've put some code for this in the file with `_LRJ_05062020.Rmd` at the end of the exploratory graphs section.  You could do something similar for poverty if you wanted.
* You are on the right track with your Poisson model for fitting a separate model for overall adolescents, and then for males, and then for females.  For these models, what you want is the number who were vaccinated as your outcome and then the sample size as your offset.  However, if you want to put males and females in to the same model with a gender variable, we will have to do a little recoding of your dataset so that you have a column for state, a column for gender, a column for poverty, etc.  This involves a little more work to rearrange your data, and wouldn't be something you would know how to do on your own.  It basically involves making your "wide" dataset into a "long" dataset.  And based on the dataset you have, it would really only allow you to look at two variables at a time (gender and poverty, gender and race, etc). 
* I think based on the complicated structure of your data, at this point I would recommend fitting separate models for a few different groups and then comparing the rates when you adjust for the political leanings variable.  I have included code for doing this for gender among the 13-17 age group.  I think there are some interesting things there when you compare the effect of political leaning on overall vaccination rates and then separately for male rates and female rates. Take a look; I've left some interpretation in the comments.
* You could also do this for poverty groups instead of gender groups.  And you could put in the advDem variable instead of the leaning variable as well.
* I hope this gets you started on some modeling.  Please reach out if you have questions as you're working through this, but I think these models will add to your graphs and make a very nice project!

##### Comments from Dr. T (4/23/2020): 

* Given how late we got comments to you last week, it looks like you have not made any changes since the version I reviewed and commented on. Feel free to reach out as you make further progress if you want additional guidance or have questions!



##### Comments from Dr. T (4/17/2020): 

* You made some nice progress this week, Lucy! 
* I spent some time fiddling around with reading in and labeling your data, before I realized you only want to focus on the 13-17 age group. I have included some additonal lines of code (in a chunk labeled dataFull) to get the full data set in a workable format in the version of your project with my initials _MAT appended. So if you want to, you can take a look at this, or just ignore it. I did also make some changes to even the simpler set of data you wanted to use, in a chunk called dataSimple.
* Are you planning on incorporating some additional state-level data in your analysis? You'll see that the political leaning data needs to have some further cleaning done to make the state names match up properly. And the same will probably need to be done for any additional state-level covariates you want to incorporate. The function toupper() is useful as a starting point since it at least makes capitalization consistent. But there are other issues like state abbreviations that have to be dealt with.
* I fixed your plot so that the bars show blue, red and grey colors. I think the issue was just that you had the leaning variable in quotes and you should not have. But I also don't think you were matching up the states and the leanings correctly, so hopefully with the left_join function this should be better now (with the exception of the state names that don't match between the two data sets).
* You will want to review the materials on Poisson regression that Dr. Jager posted earlier this week. It will be useful for your modeling.


##### Comments from Dr. T (4/6/2020): 

* Nice start, Lucy!
* It looks like this data set will require some processing/wrangling. You need to skip a couple of lines when you are reading it in, but then only select certain columns, and it is not clear to me in looking at the csv file exactly what questions and responses are being recorded. Also, some states seem to have more than one measurement (i.e., some have measurements for specific counties) so that will also need to be dealt with.
* Maybe you have already done this, but if you click on the "2018 Dashboard" link on the website you gave, it helped me understand what is in the csv file. Apparently, they need more than one dose of the vaccine. Perhaps you want to just use the rates of people who are "up to date" on the vaccine? (Starts in column HJ if you open the csv file in Excel.) I'm happy to explain more what I mean by this in office hours or over email.
* I understand that you might want to include additional variables, but given that the data set itself is a little complicated to begin with, perhaps you can just start with looking at the relationship between vaccine rates and poverty, since those variables are both contained here?
* I think this question is really interesting and it looks like a cool data set!
