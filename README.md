# Advanced Kickstarter Analysis

## Analyzing Kickstarter data to learn about success rates at different goal amounts

At the request of the client, we set out to determine with greater specificity the Kickstarter launch dates and goal amounts for plays that are most likely to find success. What follows is an explanation of the methodology we used to make those determinations, the challenges we faced and how we overcame them, the outcomes we found, and the recommendations we make based on the results of our analysis. 

## Analysis and Challenges 

### We first set out to determine if there were certain months of the years that are better for launching a successful campaign. 
To do this, we used the YEAR() function in Excel to isolate the months that campaigns for plays were launched. We did this based on Unix date data we had converted previously. We isolated the Month of Launch and assigned the data to a new column in a pivot table we created, in which we further assigned columns for data on the number of successful, failed and canceled campaigns for each month of the year. We included a column and row with grand totals.

### We then set out to determine if there were certain goal amounts that correlated to successful campaigns. 
Using the COUNTIFS() function in Excel, we totalled the number of successful, failed and canceled campaigns at 12 different goal levels:

![image](https://user-images.githubusercontent.com/4724180/146822750-699efeff-b1e7-4db4-a9e5-724a3c9d4a04.png)

### We also used the COUNTIF() totals to determine the percentage of successful, failed and canceled campaigns at each of our 12 cohorts. 
We used this data to populate a line graph illustrating the percentage of successful and failed campaigns at our 12 goal amount levels: ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/4724180/146823238-5b5e2bae-112e-40bd-925c-a8f5373f1de9.png)


### Analysis of Outcomes Based on Launch Date
We learned that the most successful campaigns were launched in May or June. The rate of successful campaigns was substantially higher in those months, and the graph that follows illustrates a spike. The rate of failed campaigns was also somewhat higher during those months, but not to the degree that the rate of successful campaigns increased. It is not clear why so many campaigns are launched during those months. 

<img width="361" alt="image" src="https://user-images.githubusercontent.com/4724180/146835155-1b1a0483-0a7f-49a8-9f12-7334247cc216.png">


### Analysis of Outcomes Based on Goals
We found that, generally speaking, the campaigns most likely to succeed were those with more modest goals. By a wide marging, campaigns with goals below $5,000 were more likely to succeed. An earlier analysis found that half of campaigns that were successful had goals between $1,500 and $5,000.

### Challenges and Difficulties Encountered
One challenge we encountered is that the YEAR() function can also be used to isolate months, which struck this writer as a little counterintuitive; is there not a MONTH() function? Ultimately, it is more convenient to have a formula that is more versatile than the its name suggests, but it did lead to some confusion for this relative newcomer.

Another challenge was populating the Outcomes Based on Goals cells with the appropriate formulas. We ended up populating each cell more-or-less manually, which required a fair amount of time and attention. This writer suspects the existence of a shortcut yet unknown.

## Results

- Campaigns launched in the months of May and June have greater success rates than those launched during other months. The number of failed campaigns also increases during those months, but not to the degree of increase of successful campaigns.

- Campaigns with lower goal amounts are more likely to meet funding goals.

- This dataset doesn't take into account possible cultural phenomenon that might also help us understand an increase in successful campaigns during the months of May and June. Because the number of campaigns launched in total during those months is significantly more than in other months, this writer has questions surrounding the data. The dataset also cannot account for the content of the proposed play and whether that content is "valuable" in such a way that it might garner greater support. For instance, there is no way to discern from our data if a play that portrays Winston Churchill in a flattering light has a greater chance of success than a play that portrays Adolf Hitler in a flattering light. One would suspect the two hypothetical plays have different chances of success for reasons that have nothing to do with the amount of their goals or the season of their launches.

- Some possiblities for further exploration of this dataset include whether a play is supported by more or fewer donors, and whether a campaign has a longer or shorter span between launch and deadline.
