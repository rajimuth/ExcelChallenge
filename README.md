# Kickstarting with Excel

## Overview of Project

### Purpose
* Louise wanted to start a crowd funding project to fund her play "FEVER", with an estimated budget of over $10,000. 
* Initial analysis was done using the available Kickstarter data including campaign categories, Campaign Goal amount, Campign Pledged amount, Countries and Campaign outcomes including Theatre/Play to explore more on specific factors that made project campaigns successful. 
* Initial analysis showed that the Theatre Category had more successful outcome followed by Music
* Initital analysis also showed that within Theatre Category, Plays had more successful outcome and that months after March in a year had successful outcomes in the past
* After the initial analysis, Louise moved ahead with the plan and started the crowd finding campaign for her play FEVER
* Louise's play Fever came close to its Fundraising goal in short time. 
* In the current analysis, we want to further analyze and visualize how different campaigns faired in relation to campaign launch dates and funding goals.

### Analysis of Outcomes Based on Launch Date
* Analysis of this data was done using Excel - pivot table and visualized using Line Chart
* Before the pivot table was inserted, the launch date that was in unix stamp format in the data set was converted to regular date format.
* Formula to convert Unix stamp to regular date was obtained using google search and then converted to short date format.
* The formula used was (((cell position of unix stamp/60)/60)/24) + DATE(1970,1,1)
* Year from the date was then added to an empty column using the year() formula
* Pivot table was inserted with the Launch date (in months) as X*axis and Outcomes (successful/Failed/Canceled) as Y axis, year and category as filters
* Theatre Category was then filtered as we are specifically interested in getting more information on this category
* This data was then used to create Pivot chart for visulaization
* Line chart was the choice as the data is a continuous data (series of month)


### Analysis of Outcomes Based on Goals
* In this analysis a new table was created using self populated values from the kickstarter data
* The number of outcomes (successful/failed/canceled) is set as columns and different range of campaign Goal amount is set as Rows
* The column values were populated using the COUNTIFS function to count the total number of Successful/Failed/Canceled campaign in the goal range and in the Play subcategory.
* Formula used was:COUNTIFS(Kickstarter!D:D, "Value of range from the row", Kickstarter!F:F, "=successful/failed/canceled", Kickstarter!S:S, "=plays")
* Percentage of successful/failed/canceled campaigns was then calcuated from the number of successul/failed/canceled campaigns in each goal range to the total number in each row (Goal range).
* The data was visulaized using line chart as the the data was continuous (range of numbers)

### Challenges and Difficulties Encountered

* One of the challenge in analyzing the Outcomes Based on Launch Date  was during the date conversion from unix stamp format
* I had to google more information on this date format and when the formula was applied the values was still in decimal 
* I had to make sure the format of the column was date and not general to view it as short date
* A possible challenge would have been encountered if Line plot was not used and if  different chart type like Bar chart or column chart was used.
* As the data in the pivot table is a continuous data it makes so much sense to use Line chart which is the best fit to visulaize this kind of data
* Challenge in Analysis of Outcomes Based on Goals was when self populating the values in the table.
* Though the COUNTIFS funtion is straight forward, extra diligence was need to make sure right criteria ranges are selected and that all the criterias were provided (goal range, outcome, subcategory"play".


## Results
### Conclusions about the Outcomes based on Launch Date
* The best time of the year to launch a campaign was after April when the number of successful campaigns was high until July.
* There was no corelation between the canceled campaigns and the Launch date

### Conclusions about the Outcomes based on Goals
* Campaigns with fundraising goals of smaller amount (less than $5000) had higher chance of success. 
* There was also a peak in success in the goal range of $35,000 * $40,000

### Limitations of this dataset
* The data set should have had information on when successful campaigns reached their goal
* This would have helped us to see what the average duration was for the other successful campaigns to reach their goal
* The second analysis was done after Louise launched her campaign and reached her goal in a short amount of time
* It would have been nice to have more information on what her campaign goal was?, When she launched it? and How long it took for her reach her goal?
* The conclusion on Outcomes based on goals suggested that smaller goal amounts had higher success rate.
* But there was also higher success in the the goal range of $35,000 *$40,000. 
* Further analysis of this goal range to explore more on statistics and outliers of the data range can provide additional insight

### Other possible tables and/or graphs that we could create?
* Country vs Outcomes (to find out which country had high successful campaigns)
* Country vs Backers count (to find out which category had higher number of backers)
* Category vs Count of Countries (to find out which category was popular in all the countries)
* Sub*Category vs Count of Countries (to find out which sub*categroy was popular in all the countries)
* Countries vs Goals amount
* Countries vs Pledged amount


