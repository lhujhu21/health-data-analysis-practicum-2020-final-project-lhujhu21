# final-project

##### Comments from Dr. Taub (4/17/2020): 

* You made some nice progress this week, Lucy! 
* I spent some time fiddling around with reading in and labeling your data, before I realized you only want to focus on the 13-17 age group. I have included some additonal lines of code (in a chunk labeled dataFull) to get the full data set in a workable format in the version of your project with my initials _MAT appended. So if you want to, you can take a look at this, or just ignore it. I did also make some changes to even the simpler set of data you wanted to use, in a chunk called dataSimple.
* Are you planning on incorporating some additional state-level data in your analysis? You'll see that the political leaning data needs to have some further cleaning done to make the state names match up properly. And the same will probably need to be done for any additional state-level covariates you want to incorporate. The function toupper() is useful as a starting point since it at least makes capitalization consistent. But there are other issues like state abbreviations that have to be dealt with.
* I fixed your plot so that the bars show blue, red and grey colors. I think the issue was just that you had the leaning variable in quotes and you should not have. But I also don't think you were matching up the states and the leanings correctly, so hopefully with the left_join function this should be better now (with the exception of the state names that don't match between the two data sets).
* You will want to review the materials on Poisson regression that Dr. Jager posted earlier this week. It will be useful for your modeling.


##### Comments from Dr. Taub (4/6/2020): 

* Nice start, Lucy!
* It looks like this data set will require some processing/wrangling. You need to skip a couple of lines when you are reading it in, but then only select certain columns, and it is not clear to me in looking at the csv file exactly what questions and responses are being recorded. Also, some states seem to have more than one measurement (i.e., some have measurements for specific counties) so that will also need to be dealt with.
* Maybe you have already done this, but if you click on the "2018 Dashboard" link on the website you gave, it helped me understand what is in the csv file. Apparently, they need more than one dose of the vaccine. Perhaps you want to just use the rates of people who are "up to date" on the vaccine? (Starts in column HJ if you open the csv file in Excel.) I'm happy to explain more what I mean by this in office hours or over email.
* I understand that you might want to include additional variables, but given that the data set itself is a little complicated to begin with, perhaps you can just start with looking at the relationship between vaccine rates and poverty, since those variables are both contained here?
* I think this question is really interesting and it looks like a cool data set!
