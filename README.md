# Kickstarter Analysis

By Nicholas Labinski

## Overview

**Purpose of the Project**

My friend Louise wants to launch a Kickstarter campaign for a play she wants to put on, *Fever*. *Fever* came close to reaching its fundraising goal in a short amount of time. Now, Louise has contacted me to analyze Kickstarter data that was collected from 2009 to 2017 to determine how different campaigns fared in relation to their launch dates and their fundraising goals. The data set is large, including data on the goal of the campaign, the amount pledged, country, date launched/completed, and number of backers, among the data most pertinent to this analysis. This data includes information on plays and other theatrical campaigns, as well as campaigns for books, television, music, and more. Louise would like me to analyze the data so she has a better understanding of the fundamentals that might shape a successful, or unsuccessful, Kickstarter campaign. She believes it is critical to understand when campaigns are launched, the type of campaign, including unique campaigns, and how campaigns for plays, her interest, faired. This analysis is intended to help Louise understand the fundamentals of Kickstarter campaigns, provide insight about launch dates, the campaign goal, and their influence in the success or failure of play campaigns.



## Analysis and Challenges

**Analysis**

This section will overview some of the basics in preparing the data for analysis. 

With a large dataset, one of the keys to a successful analysis was filtering the data to better match Louise's goal. This filtering included creating Parent Category and Subcategory sorting tools that allowed me to focus my analysis on theater campaigns, and to dive even deeper into the data with a sharper focus on only plays. Additionally, extra columns were added to convert the unix timestamps to regular dates, for a clear understanding of when campaigns launched and concluded, and a year column was included for quicker reference and ease of sorting in pivot tables.

From there, my first major analysis was to filter the data, examining all theater related campaigns over the eight year period. A pivot table was created (below), showing the successful, failed, and canceled campaign totals for each month, with the campaign outcomes sorted in descending order so "successful" is first. To generate the pivot chart, I put the fields of Parent Category and Years into the filters box, in the Legend box went the Outcomes field, in the Axis box went the Data Created Conversion field, and in the Values box went the Count of Outcomes field. The data would allow Louise to see which months, if any, launched the most campaigns, which months were more successful, and which ones were not. Drawing on the data in this pivot chart, a clear visualization of the data was created in a line graph (see below in the results section for the chart and discussion). <img src="https://github.com/labinskin/Kickstart-Analysis-to-Find-Trends/blob/main/Pivot%20Table.png" /> 

The second major analysis presented in this report was the collection and analysis of data pertaining to the funding goal amount of plays. Using the `=CountIfs`function in Excel, data was transferred from the main spreadsheet to a new one. The data was arranged in rows and categories. The rows consisted of possible goal amounts starting with less than $1,000, then $1,000 to $4,999, and increasing in increments of $4,999 until the last category of $50,000 and above. The columns consisted of `=CountIfs`that totaled the number of successful, failed, and canceled campaigns. Another column totaled the projects with the `=Sum`function. And the last three columns calculated the percentage of successful, failed, and canceled campaigns. ![Outcomes Chart](https://github.com/labinskin/Kickstart-Analysis-to-Find-Trends/blob/main/Outcomes%20Chart.png)This allows Louise and us to examine if there are goals amounts that are more or less successful. A full visualization of the data is presented below in the results.

**Challenges**

There was only one major challenge faced in this analysis, outside of forgetting an equal to sign for the $50,000 row, was reorganizing the data in the pivot chart for the first set of analysis. When the pivot chart was originally created, the data was grouped by quarter, not month. I had to figure out how to ungroup the data by quarter. To do this, under the PivotTable Analyze tab, I used the Group selection to determine how the data was shown. I unclicked the boxes that were not months and the data was appropriately grouped after.

## Results

**Conclusions**

Based on the Theater Outcomes Based on Launch Date Pivot Table (above) and Visual Representation (Below), there are a couple of conclusions that can be drawn. ![Theater_Outcomes_vs_Launch](https://github.com/labinskin/Kickstart-Analysis-to-Find-Trends/blob/e5f9525bf089a129c80724338c701683b676a517/Resources/Theater_Outcomes_vs_Launch.png)



First, the spring and summer months of April through August are the busiest months of the year for Kickstarter campaigns for plays, with May and June being the busiest. These months also had the highest number of successful Kickstarter campaigns, with slightly higher failure numbers too. However, the difference in the months of May and June were not as significant compared to other months, with May and June only having a few more failed campaigns. Therefore, it would seem that May and June would be good months to launch a Kickstarter campaign for a play. On the opposite end of this trend were the months of October through January. These months had a lower total number of launched campaigns and the success/failure numbers were closer together. Therefore, it would be recommended to not launch a Kickstarter campaign for a play in these months.

The second set of conclusions will be drawn from my analysis based on Goal Outcome (see visualization below)

![Outcomes_vs_Goals](https://github.com/labinskin/Kickstart-Analysis-to-Find-Trends/blob/e5f9525bf089a129c80724338c701683b676a517/Resources/Outcomes_vs_Goals.png)

Based on the analysis of the chart and graph, there is a clear recommendation for playwrights to be careful about not going over the $4,999 goal threshold. Plays under that threshold were funded approximately 75% of the time, while plays above the threshold were closer to a 50% chance of being funded successfully. An exception is in the $35,000 to $44,999 range. However, when looking at the raw data (see chart above), it is clear that there are only a total of 9 projects here, compared to 720 for $4,999 and under. Simply, the sample size on the higher range is too small to draw a definite conclusion that it will be funded.

Overall, from the two charts and graphs, the data makes clear that setting a goal for $4,999 and under with a campaign launch date in May and/or June or a month or two on before May or after June has the highest likelihood of success. While campaigns with higher goal outcomes launched during a different month, but especially October through January are less likely to succeed.

**Data Limitations**

There are a few limitations to the data that must be noted. First, the dataset only includes data up to 2017. We are almost four full years past the last piece of data collected. In this time, the world has undergone and is in the midst of a global pandemic that has shifted our ability to engage in theater, especially plays. While some countries, including the United States, have begun a return to normalcy, the global pandemic could have changed the success/failure rate of Kickstarter campaigns, especially theater and plays. Additionally, economic hardship of many citizens around the globe could influence the number of campaigns that get fully funded.

Second, there is little information about supporters outside of the average donation. More demographic information about supporters would be critical. What demographics typically support theater and play Kickstarter campaigns? Collecting and analyzing any demographic information about supporters might be critical in crafting and launching a successful campaign. There could be a specific demographic of donors that fund a majority of campaigns. Targeting this demographic could be critical in funding a campaign.

Third, does the genre of the play matter or influence its success or failure? Each play has a blurb, describing what takes place. But, there is no genre category. Could the content of the play influence the amount donated, effecting which plays succeed and fail?

Fourth, there is no information about advertising and social media campaigns to publicize the campaigns. Understanding how the organizers publicized the event and the reach these efforts have could be a factor in determining the success or failure of a campaign. If an organizer was able to publicize their campaign to a wide audience, they could garner many supporters and meet their goal. However, if a campaign was poorly publicized or relied on people searching and looking through the vast amount of Kickstarter campaigns to stumble upon theirs, with few people knowing it existed, could be another factor in its success or failure. This might be one of the easier data points to collect and add to the analysis. Asking Kickstarter if they collect and maintain data on the number of individual and unique user page views for each campaign could bring in a haul of new data to analyze. By collecting that data, an analysis could be conducted to see if the number of page views influences the success or failure of a campaign.

**Additional Analysis**

Another chart and analysis would be to create and cross reference the data between month of launch and outcome based on goals. This type of analysis would examine and provide insight into if the successful campaigns in May and June were due to just the pure number of campaigns launched or if there was a correlation between successful cheaper May/June campaigns and more expensive May/June campaigns that failed.

As work was done on the Mean, Median, Standard Deviation, and IQR of the Goal and Amount Pledged, adding additional graphs and charts on this data would help visualize the data better for Louise. Furthermore, a table, graph, and analysis of the Pledged Amount data in the vein of Outcomes Based on Goals analysis presented above would helpful in visualizing and analyzing this data.

Last, the possible addition of new data about unique and individual page views would lend deeper insight. This data would need to be collected, but many websites track such information. Getting this data would allow pivot tables and charts to be created, providing deeper insight into Kickstart campaign success or failure.
