# Kickstarter-Analysis

## Overview of the Kickstart Analysis

### Purpose of Kickstart Analysis
The purpose of the analysis is to assist Louise to determine how different campaigns fared with relation to the campaign’s launch date and fundraising goals.   The following data focuses on what effect each month had on the Theater Campaign.  The other part of the analysis goes further into the Theater Campaign looking into the impact of plays at different levels of funding goals.

## Analysis and Challenges

### Analysis of Outcome based on Launch Dates
The first analysis looked at successful, failed, and canceled campaigns by month using a pivot table and line chart.  We created filters to look specifically at the theater campaign and used the years columns to convert to months. 
![image](https://github.com/ExcelChallenge1/Theater_Outcomes_vs_Launch.png)
### Analysis of Outcomes Based on Goals
Our next analysis was to determine the impact different levels of funding goals could have on outcome of plays within the Theater campaign.
![image](https://github.com/ExcelChallenge1/Outcome_vs_Goals.png)
### Challenges and Difficulties Encountered
One challenge was creating a Years column in the dataset.  We began by creating a column for Date Created Conversion because the original column for beginning dates contained UNIX timestamps and had to be converted with the Date formula. =(((J2011/60)/60)/24)+DATE(1970,1,1)
After pulling the created date we used the YEAR() function which allowed us to change the column to the beginning month of each campaign.  =YEAR(S2011)
The challenges were working through the COUNTIFS() to lock the criteria range, and correctly change criteria 2 from Successful, Failed, and Canceled outcomes.  Also, to make sure to use Plays as criteria 4.  =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Failed",Kickstarter!$R:$R,"Plays")
I worked my way through how to lock the columns with a little trial and error with function F4.  I realized Plays was criteria 4 after readdressing the question.
I also experienced challenges with the text on pivot table Headers and how to remove “Grand Total” row.  I adjusted the headers by replacing the text I didn’t want displayed with one click of the space bar and it held the correct header.  To remove the “Grand Total row, I clicked Design Tab then clicked the drop-down arrow of the Grand Totals tab, then clicked “Off for rows only”.
When I created the Line Chart values kept showing up on the data points of my lines.  I manually removed the value by double clicking anywhere in the line chart to open Format Data Label window.  I clicked “label options” then click the arrow down under “label options” and clicked value.  Unfortunately, every time I open the worksheet in refills the value, so I haven’t found a permanent solution.

## Results
The two conclusions I drew on from the Outcomes based on Launch Date were:
- The summer months (May, June, July) indicate to be the more successful months to begin a theater campaign.  May being the most successful.
- October and December appear to be the most unsuccessful months to begin a theater campaign.  Almost 50% failed.

Parent Category	theater			
Years	(All)			
				
Count of outcomes	Column Labels			
Row Labels	successful	failed	canceled	Grand Total
Jan	56	33	7	96
Feb	71	39	3	113
Mar	56	33	3	92
Apr	71	40	2	113
May	111	52	3	166
Jun	100	49	4	153
Jul	87	50	1	138
Aug	72	47	4	123
Sep	59	34	4	97
Oct	65	50		115
Nov	54	31	3	88
Dec	37	35	3	75
Grand Total	839	493	37	1369

- My conclusion on the Outcome based on Goals shows that higher goal amounts did not make plays more successful.

Row Labels	 Percentage Successful	 Percentage Failed	 Percentage Canceled
 Less than 1000	76%	24%	0%
1000 to 4999	73%	27%	0%
5000 to 9999	55%	45%	0%
10000 to 14999	54%	46%	0%
15000 to 19999	50%	50%	0%
20000 to 24999	45%	55%	0%
25000 to 29999	20%	80%	0%
30000 to 34999	27%	73%	0%
35000 to 39999	67%	33%	0%
40000 to 44999	67%	33%	0%
45000 to 49999	0%	100%	0%
Greater than 50000	13%	88%	0%

- Limitations with the dataset:
	1.  Not able to determine what was driving the variance from month.
	2.   Not easily able to identify differences in types of plays.
	
- Additional Charts:
	1.  Histogram
	2.  Box & Whisker
