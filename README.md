# Kickstarting with Excel

## Overview of Project
To illustrate the power of excel to perform various analysis on large data sets. The aim is to get a better understanding of the hidden trends and truths to help us make informed choices. We are using an illustrative example of a project for Louise an upcoming playwright for the purpose of this project. 
Louise wants to launch her first play Fever. She estimates that the production of her play will cost upwards of USD 10,000 and wants to fund it through a crowd funding campaign on Kickstarter. This being her first crowd funding campaign she is a little unsure. She has requested us to study the various crowd funding campaigns and advise her on the best way forward.

### Purpose
The main purpose of this exercise is for us to get a good understanding of the crowdfunding campaigns as a whole and specifically the crowdfunding campaigns in the United States, in the category theater and subcategory plays. Based on past campaign data we want to understand the following                                                                                                                                                                                                                                                                                                                                                                                                                    
-	Are crowd funding campaigns a good option for the category/sub-category of theater/plays?       
-	How have crowdfunding campaigns fared historically in terms of achieving their funding goals?
-	What is the rate of success of such campaigns?
-	What are the factors that affect success of crowdfunding campaigns?
-	What are average donations and number of backers that one can expect in such campaigns?
-	What is the best time of the year to launch this campaign? 

Our final purpose is to provide Louise with insights and trends that will help her make informed choices for her campaign.

## Analysis of Project
We begin our analysis with a data set containing campaign details of 4000+ Kickstarter campaigns. These campaigns span a few years, are across various campaign categories/sub-categories and also across markets. We quickly massage the data to uncover some broad insights
-	Since we are interested in a specific sub-category of plays – we split the category/sub-category column into two separate columns so that we can analyze plays specifically
-	We computed the % funded column from the goals and pledged amount for each campaign
-	We computed the average donation amounts per campaign 
-	We color coded the outcomes column with different colors – green for successful, red for failed, blue for live and yellow for cancelled campaigns for easy reading  
-	We used color gradient to indicate the range of funding with red for lower % funded to blue for higher % funded for easy identification. 
-	We converted the campaign start date and end dates to a readable format.
-	We added a year of campaign column from the date column

### Our initial findings are 
-	54% of all Kickstarter campaigns are successful and 38% failed 

![image](https://user-images.githubusercontent.com/85518330/122474760-45982480-cf89-11eb-8a15-4394323596dd.png)

 
-	Theater is the most popular category for Kickstarter campaigns and accounts for 34% of total number of campaigns
 

 ![image](https://user-images.githubusercontent.com/85518330/122449403-6d788f80-cf6b-11eb-9bd3-b5de9e51f98b.png)


-	Plays is the most popular sub-category in the theater category and account for 76% of all campaigns. 


 ![image](https://user-images.githubusercontent.com/85518330/122451260-8c782100-cf6d-11eb-866a-f729e723561f.png)


-	66% of plays on Kickstarter have had a successful outcome


 ![image](https://user-images.githubusercontent.com/85518330/122450245-68681000-cf6c-11eb-8be2-df7a563a5217.png)


### Analysis of Outcomes Based on Launch Date
This analysis helps us understand the relation between the month of campaign launch to its successful outcome. 
This analysis will help us advise Louise on the best times of the year to launch her campaign. 

For this analysis we followed the below steps
-	Converted the campaign start and end dates from the Unix time stamps to more readable ones
-	Then we created a pivot table by filtering data by years and categories
-	We filtered the categories to include only theater 
-	Excel automatically parsed the date information to give us options of months or quarters.
-	We selected months so that we could clearly see if there was any seasonality to the campaigns


![image](https://user-images.githubusercontent.com/85518330/122445912-ad3d7800-cf67-11eb-9540-9e780ab2b6a3.png)


### What are two conclusions you can draw about the Outcomes based on Launch Date?

- Theater campaigns launched May through July have a higher success rate
- End of the year is a bad time to launch campaigns for theaters/plays 


### Analysis of Outcomes Based on Goals
Here our aim is to find the impact of goal amounts on campaign success for the sub-category plays.

For this exercise we created certain goal ranges to help bucket the campaigns based on their funding goals
-	We used the Countifs function to help us populate the numbers of campaigns based on their outcome into their corresponding buckets 
-	What we got was an easily readable table, we went ahead and further computed the % from the numbers 
-	We created a line graph with the information in the % table that we could see and interpret easily


![image](https://user-images.githubusercontent.com/85518330/122446242-0efde200-cf68-11eb-9b4b-8679cc5ea34b.png)


### What can you conclude about the Outcomes based on Goals? 

- Lower goals of less than 5000 USD have the highest rate of success and form a majority of all play campaigns on Kickstarter
- Plays with higher goals of between 35000 & 44999 USD also had a high success rate but these were very few in number and hence not a significant sample

### Challenges and Difficulties Encountered
-	I felt that the data set provided to us for the purpose of this exercise was somewhat limiting. Having more information on reasons why campaigns failed of were cancelled could help us analyze a comprehensive list of reasons/pitfalls for Louise to be cautious about
 
## Results
Our analysis uncovered the following insights that we would share with Louise 

-	Theaters/plays are a popular category for running fund raising campaigns on Kickstarter
-	May through July is a good time to launch her campaign
-	Most successful plays have had funding goals of 5000 USD or less, plays with higher goals have failed more. 
-	However, when we check data on outcomes based on actual pledged amounts, we find that successful campaigns had higher pledged amounts than failed campaigns. 
-	Our descriptive analysis points to the fact that higher funding goals is not the only reason that has caused campaigns to fail 

![image](https://user-images.githubusercontent.com/85518330/122473157-1385c300-cf87-11eb-8d2f-8b3b017f9d85.png)

-	So, while prima facie a funding goal of 10000+ USD that Louise is seeking seems high. We will need to do some further research to try and find out other factors that may cause campaigns to fail. Before we recommend lowering her funding goals

## What are some limitations of this dataset?
- We know some campaigns failed and some were canceled, we don’t however know the exact reason why the campaigns failed or what caused the campaigns to be canceled. 
- This limitation is forcing us to analyze our campaigns outcome purely from the stand point of funding goals and amounts pledged. 
- This is leading to an indication that Louise may be seeking a higer than recommended funding goal for her campaign. This may or may not be the entire truth and there could be other reasons for campaign failure which we are currently ignoring

- It may have helped us if we could deep dive more into the plays subcategory to understand the genres that the various plays belonged to. We may have then been able to guide Louise better on her Comdey play Fever 

## What are some other possible tables and/or graphs that we could create?
- Tables and graphs correlating campaign outcomes based on average donations the campaign generated 
- Correlation between campaign outcomes and number of backers it had
- The impact of staff picks on campaign outcomes
- Impacts of campaign duration on outcomes




