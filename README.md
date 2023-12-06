# MIST4610-GROUP-PROJECT-2

## Group name

39217 Group 5

## Team Name

Megan Gentles [@megangentles](https://github.com/megangentles)

Lindsay Kilpatrick [@lindsaykilpatrick](https://github.com/lindsaykilpatrick)

Aaron Phelps [@aaronphelps](https://github.com/aphelps94)

Hailey Trivedi [@haileytrivedi](https://github.com/haileytrivedi)

Sahana Solipuram [@sahanasolipuram](https://github.com/sahanasolipuram)

Paige Sawyer [@paigesawyer](https://github.com/paigesawyer)



## Description of Data Set

The dataset used in this project contains information on motor vehicle collisions in New York City from 2013 to 2023, and it was last updated on December 2nd, 2023. This dataset was obtained through data.gov and specifically the catalog of various datasets (https://catalog.data.gov/dataset/motor-vehicle-collisions-crashes). It is worth noting that this dataset comes from police reports on the collisions, which are only required to be filled out if someone is injured or killed in the collision or if there is at least $1000 worth of damages. Our dataset has a variety of different data types present within it, including date and datetime in order to document when the collision occurred. There is also geographic data for latitude, latitude and zip code. Finally, we have multiple string fields for up to five contributing factors or vehicles involved in the collision and numbers to keep track of how many individuals are injured or killed both in general and broken down among cyclists, motorists and pedestrians specifically. This variety of data types and their amount allow us to take a deep dive into determining many different factors behind these collisions in the hopes of reducing the frequency and severity of them over time.



## Questions

### Question 1

Question: Is there one area of the city that contains the majority of motor vehicle incidents? What is the relationship between the vehicle type involved in an accident and the number of those injured? 

Importance:

The NYC motor vehicle accident dataset that we decided to utilize breaks down where each accident occurred, as well as which vehicle type was involved in the accident, both of which would be needed to thoroughly respond to this question. Car accidents are the leading cause of death in United States citizens under the age of 54, so any preventative measures should be taken to reduce the annual volume of car accidents. This question is important to consider because there may be factors in certain areas of the city, such as road conditions or construction, that are contributing to an increased number of accidents. If lawmakers could pinpoint a reason behind the increased number of accidents, steps could be taken to reduce the number of accidents in that particular area of the city. Vehicle type is also interesting to consider because if only certain types of vehicles, such as taxis or trucks, are involved in a large number of accidents, preventative legislation could be put in place to prevent as many accidents as possible moving forward. 

Analysis:

From the data, there does not appear to be one particular area that stands out. It seems that accidents are spread evenly throughout all of the boroughs of New York City. There tends to be, however, a large number of Sedans and station wagons that are involved in accidents and produce the most injuries. Interestingly, though, the incidents involving taxis seem to be mainly confined to Manhattan. Lawmakers can now take this information to know that one area is not necessarily more prone to accidents than others. They can also make more legislation and restrictions surrounding sedans and station wagons moving forward to prevent further accidents.



<img width="632" alt="Screenshot 2023-12-05 at 9 33 27 AM" src="https://github.com/haileytrivedi/MIST-GROUP-PROJECT-2/assets/149614680/8720f687-a5c9-4f39-add4-2398e2001117">



### Question 2

Question: Are motor vehicle incidents more prone to occurring in certain months versus others? Are the amount of people injured in an incident correlated to the total number of accidents?

Importance:

As previously mentioned, car accidents are the leading cause of death in US citizens under the age of 54, so it is important for lawmakers to look for patterns in accident data and try to put in place preventative policies in any area possible. This question is interesting, as there may be seasonal factors that are influencing the number of accidents. It will be interesting to see if there is a pattern to see if most accidents take place in the winter when there might be turbulent weather conditions or if seasonal factors do not hold a large stake in this data. After that is determined, the severity of the accident should be measured in the different months as well, to see if seasonal factors play a part in how many people are injured/killed. It would also be interesting to see if a larger volume of accidents in a certain month automatically leads to a larger amount of people injured/killed. Once all of this information is determined and any patterns are detected, lawmakers can then work on decreasing seasonal patterns and reducing accident-causing factors that can be controlled.

Analysis:

We discovered that September has historically had the highest number of crashes, followed by March and April. The sum of total injuries per month positively correlated with the total number of crashes per month, as September and March had the most amount of people injured. The sum of people killed in motor vehicle incidents does not seem to be related, as someone dying in a car accident is rare compared to injuries.



<img width="633" alt="Screenshot 2023-12-05 at 9 33 06 AM" src="https://github.com/haileytrivedi/MIST-GROUP-PROJECT-2/assets/149614680/02ba554e-e923-4595-ab6a-0f17afd17522">


## Manipulations Applied

Before uploading the dataset into tableau, we limited the rows to 500 rows to cut down the amount of storage and computer power needed to run analysis on the data. For the map visualization, a manipulation and calculation was performed on the data. First, we only included the following vehicle types as they were the most common types and provided the significant data points: box truck, bus, e-bike, motorcycle, pick-up truck, sedan, station wagon/sport utility vehicle, and taxi. Additionally, we calculated the total number of people injured by adding together: 

[Number Of Persons Injured]+[Number Of Motorist Injured]+[Number Of Pedestrians Injured]+[Number Of Persons Injured]. 
	
 
 For the visualization with three charts, numerous calculations were made to create this. The same injured calculation was done as well as the sum of those killed. Numerous calculations were used to create the data regarding the contributing factor for the motor vehicle accident. In the data source tab, we counted the number of instances if the data included “Alcohol,” “Unsafe,” “Distraction,” “Too Closely,” or “Aggressive Driving.” For alcohol the code was the following: 

COUNT(IF CONTAINS([Contributing Factor Vehicle 1],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 2],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 3],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 4],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 5],"Alcohol") THEN 1 END).


This code allowed us to sum the amount of those occurrences to segregate the data based on the contributing factor. This allowed us to see whether there was one dominating contributing factor. It also allowed us to visualize contributing factors on the same x-axis as the number of people injured/killed to see if there was a correlation. These manipulations allowed us to break out these factors based on month to also see if seasonality had an impact.


## Tableau packaged workbook

The packaged workbook containing the visualizations shown above is attached to this repository.

## Honors Option

## Description of Data Set

This next dataset contains information on global landslides from 1988 to 2017, and it was last updated on September 14th, 2023. This dataset was obtained through data.gov (https://catalog.data.gov/dataset/global-landslide-catalog-export). The dataset has a variety of different data types present within it, including date and datetime in order to document when the environmental event occurred. There is also geographic data for latitude, latitude, country, and country code. Finally, there are multiple string fields including an event and location description amoung others. 

### Question 1
Is there a correlation between the number of fatalities and the location of the event? Is there a relationship between event trigger or landslide size and geography? Is the a difference for landslides versus mudslides?

Importance: 

It's important to see whether certain locations are more prone to natural disasters such as mudslides or landslides and to determine if more resources need to be allocated to some areas rather than others. Additionally, knowing whether there is a common cause for the natural disaster can also help prevent them in the future and may even reduce the number of fatalities a country may have due to mudslides and landslides. Seeing a geographical visualization of this data allows for connections and correlations to be made in order for these events to be better prevented in the future and better allocate aid. 

Analysis: 

<img width="1058" alt="Screenshot 2023-12-05 at 11 17 07 PM" src="https://github.com/paigesawyer/MIST-GROUP-PROJECT-2/assets/148093138/ebbd377f-1aee-411d-9284-a4141bb0c30b">

In this visualization, it is apparent that there are various triggers to landslides, yet downpour and continous rain seem to be overwhelmingly the main reason for these natural disasters. Those are also the largest dots, showing those triggers also result in the largest landslides. As for geography, the west coast of the United States has a number of these events as well as South Asia. 

<img width="1050" alt="Screenshot 2023-12-05 at 11 14 44 PM" src="https://github.com/paigesawyer/MIST-GROUP-PROJECT-2/assets/148093138/18819c36-4d99-4ae7-82b8-ee100a626040">

This visualization can be used in combination with the above to see whether the size of the dots correlate to higher rates of fatalities. Myanmar has the highest total number of fatalities and this relates to the very large dots of continuous rain in the previous visualization. 

<img width="883" alt="Screenshot 2023-12-05 at 11 16 25 PM" src="https://github.com/paigesawyer/MIST-GROUP-PROJECT-2/assets/148093138/d220dfda-7c3b-4472-b164-d919ddbd7867">

Given the above realization, I have included a zoomed in image of the area with the highest number of fatalities. While there are a variety of triggers, rain seems to be the main cause. This shows that this area may need better drainage systems and flooding control. It would be worth spending more resources on preventing landslides here to reduce their high fatality number. 


The workbook for this dataset is attached above as HonorsOption. A dashboard was also created to see both visualizations side by side. 
