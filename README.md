# Kickstarting with Excel

## Overview of Project
Louises play Fever came close to its fundraising goal in a short amount of time. I was tasked with discovering how different campaigns fared in relation to their launch dates and their funding goals.
### Purpose
To create a report analyzing outcomes based on campaign launch dates and funding goals. 
## Analysis and Challenges
### Analysis Theater Outcomes by Lanuch Date
In the Theater Outcomes by Launch Date I began by converting the current date from Unix using the formula =(((J2870/60)/60)/24)+DATE(1970,1,1). 
Next I created a column for the year that the challenges were created using the formula =YEAR(R3846). 
With that data complete a pivot table was created using Theater Outcomes by Launch Date. The parent category and years were used as filters. The count outcomes use the months and each following column looked at canceled, successes and failures. The pivot table was sorted to show the success first in descending order. 
Lastly, a line chart was created showing the number of successful, failed, or canceled projects by month. 
![Theater Outcomes va Launch](../../../../../../c:/Users/aahud/Dropbox%20(Personal)/Bootcamp/Crowfunding%20Analysis/resources/Theater_Outcomes_vs_Launch.png)
### Analysis Outcomes Based on the Goals 
Next a new sheet was created showing Outcomes Based on the Goals. 
A chart was created with the following columns. 
Goal
Number Successful
Number Failed
Number Canceled
Total Projects
Percentage Successful
Percentage Failed
Percentage Canceled
The rows were created based on dollar ranges. 
Less Than 1000
1000 to 4999
5000 to 9999
10000 to 14999
15000 to 19999
20000 to 24999
25000 to 29000
30000 to 34999
35000 to 39999
40000 to 44999
45000 to 49999
50000 or More
To discover the counts of successful, failed and canceled campaigns in the dollar ranges the following formula was used =COUNTIFS(Kickstarter!$F:$F,"=successful",Kickstarter!$D:$D,"<=1000",Kickstarter!$P:$P,"plays") 
Then to find the percentage the number of counts was divided by the total sum of each line. To find the sum of each line the SUM function was used. 
Then results of this chart was used to create a second line chart. 

![Outcomes VS Goals](https://github.com/aahudson/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)
Outcomes_vs_Goals.png
### Challenges and Difficulties Encountered
There were some challenges creating the IF formual and getting the logic just right to pull the correct data. Help was received from an additional collegaue. 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Based on the Theater Outcomes by Lanch Date a May or June campaign  is likely to have the best success.
However, keep in mind that May, July, and October had high failure rantes of 50 and above.  
- What can you conclude about the Outcomes based on Goals?
Based on the Outcomes Based on Goals data it appears the best campaign range is in the $1,000 - $4,999 range. 
- What are some limitations of this dataset?
Every dataset has it limits. We are limited to the extent that the data was entered correctly. Outliners of either high or low numbers can also scuew the results. To view the raw data please see the following Excel file:
[label](../../../../../../c:/Users/aahud/Dropbox%20(Personal)/Bootcamp/Crowfunding%20Analysis/Kickstarter_Challenge.xlsx)
- What are some other possible tables and/or graphs that we could create?
An additional table comparing the percentage of successful campaigns compared to failed campaigns may help the decision between which month to launch. 
