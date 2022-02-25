# An Analysis of Kickstarter Campaigns

## Overview of Project
Kickstarter data has been analyzed and visualized in several ways, focusing mainly on campaign outcomes vs. goals and launch date.

### Purpose
The goal of this project was to analyze kickstarter data from a plethora of countries, categories, and goal ranges in order to help the client, Louise,
make an informed decision on how to raise money for her own theater campaign. 

## Analysis and Challenges
#### Intro to Excel
This analysis was mainly performed to become familiar with using excel. The first thing I became familiar with was filtering each column. The main challenge
I ran into with this was realizing that when removing filters from the main dataset, all graphs or pivot charts that were made from that dataset will change.
When making specialized graphs, it is probably best to copy a filtered version of the data into a new worksheet for use with any charts, that way you can 
freely edit the original data filters.

#### Lookup
The next major excel function I learned how to utilize was Lookup. I was able to use this function in the "Edinburgh Research" worksheet to easily 
reference the synopsis of each campaign we were interested in from Great Britain. 
See the function call used: `=Lookup(A2, Kickstarter! B:C, 2, FALSE)`

#### Pivot Charts
I was able to play with a few simple pivot charts, studying the number of successful, live, and failed campaigns in each category. We focused on the theater
category for this analysis:
![pivot table screenshot](https://github.com/KW0114/kickstarter-analysis/blob/621db11b96b04bfe4ba724f174e416350d6be23b/theatre_outcomes_pivot.png)
Luckily, the majority of the theater campaigns were successful. 

#### Descriptive Statistics
After playing with pivot charts and how to filter/order them, I practiced calculating descriptive statistics on my dataset. Luckily my math background
made this part of the assignment much easier. While I had no issues, I could anticipate someone with little exposure to statistical language to struggle
with what each term means in relation to the data.
![descriptive statistics screenshot](https://github.com/KW0114/kickstarter-analysis/blob/d03474a262447bfc6ff8fb8e87d7a0b16a1ee91b/theatre_outcomes_pivot.png)
Looking at these stats, we can see that each category's mean is larger than the median. This shows a right skew to our data, meaning there are most likely
some large outliers pulling the mean upward. This is further confirmed as we notice that the mean is very close to the third quartile in each set of data.

### Analysis of Outcomes Based on Launch Date
![outcomes vs launch date screenshot](https://github.com/KW0114/kickstarter-analysis/blob/2cdf709dc300ae5622b792283626d872788b2290/Theatre_Outcomes_vs_Launch.png)

Examining the line chart, we can see that the most successful theater campaigns are launched in May. While there is a steady downward trend, the months of
June and July are notably high in successful campaigns. One more notable observation is that the number of failed and successful campaigns are fairly similar from September through October. 

### Analysis of Outcomes Based on Goals
![outcomes based on goals screenshot](https://github.com/KW0114/kickstarter-analysis/blob/2cdf709dc300ae5622b792283626d872788b2290/Outcomes_vs_Goals.png)

I thought the behavior of this chart was extremely fascinating. The trend of percentage successful and failed campaigns seem to almost be perfectly mirrored.
As the goal approaches 2000, failed campaigns become more prevalent, and overtake the successful campaigns in a huge spike around a goal of 25000.
The trend completely flips around a goal of 30000, where successful campaigns overtake the failed, and plateaus from 35000 to around 40000. Once we surpass
a goal of 40000, successful campaigns plummet. 

### Challenges and Difficulties Encountered
In summary, the main difficulties I had during this analysis had to do with function syntax. I was able to learn a lot about nested function calls, and that I need to be careful
by using parentheses and commas correctly inside of functions.
It also took me quite a while to realize how useful it is to lock functions in order to keep most of the values, and only edit one or two things as I reuse it. I do have some 
experience coding in C when I was an undergraduate TA for CS1 at UCF, so things like this are slowly coming back to me.
I am also a middle school math teacher, so checking for errors carefully is something I am very familiar with, especially with calculations and coding. 

## Results

- In general, it seems that late Spring, or Summer months are the best times to begin a new campaign.
- It is difficult to accurately predict results when campaigns begin anytime from September to December, because the number of failed and successful
campaigns in this time range are fairly close.

- Campaigns with a goal of over 40000 are highly likely to fail.
- Successful goal ranges tend to be less than 5000, or from 35000 to 40000.

- This dataset seems to be very wordy, especially because each campaign includes a summary of what they are trying to promote. If the purpose is mainly to 
crunch numbers, I think deleting a lot of this information we never used would make it much easier to read.
- There also seem to be several typos or weird, random
capitalization that could make it difficult when searching for keywords, especially if we are looking for exact matches. 

- While we studied the effect of launch date on the success of a campaign, I think it could be useful to study the effect of how long a campaign ran
on its success. Do longer campaigns have a better chance of success? How does the goal play into that?
