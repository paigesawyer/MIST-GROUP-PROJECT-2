# MIST-GROUP-PROJECT-2

## Team Name

Megan Gentles

Lindsay Kilpatrick

Aaron Phelps

Paige Sawyer

Sahana Solipuram

Hailey Trivedi



## Description of Data Set




## Questions

### Question 1

Question: Is there one area of the city that contains the majority of motor vehicle incidents? What is the relationship between the vehicle type involved in an accident and the number of those injured? 

Importance:

The NYC motor vehicle accident dataset that we decided to utilize breaks down where each accident occurred, as well as which vehicle type was involved in the accident, both of which would be needed to thoroughly respond to this question. Car accidents are the leading cause of death in United States citizens under the age of 54, so any preventative measures should be taken to reduce the annual volume of car accidents. This question is important to consider because there may be factors in certain areas of the city, such as road conditions or construction, that are contributing to an increased number of accidents. If lawmakers could pinpoint a reason behind the increased number of accidents, steps could be taken to reduce the number of accidents in that particular area of the city. Vehicle type is also interesting to consider because if only certain types of vehicles, such as taxis or trucks, are involved in a large number of accidents, preventative legislation could be put in place to prevent as many accidents as possible moving forward. 


<img width="633" alt="Screenshot 2023-12-05 at 9 33 06 AM" src="https://github.com/haileytrivedi/MIST-GROUP-PROJECT-2/assets/149614680/02ba554e-e923-4595-ab6a-0f17afd17522">


### Question 2

Question: 

Question: Are motor vehicle incidents more prone to occurring in certain months versus others? Are the amount of people injured in an incident correlated to the total number of accidents?

Importance:

As previously mentioned, car accidents are the leading cause of death in US citizens under the age of 54, so it is important for lawmakers to look for patterns in accident data and try to put in place preventative policies in any area possible. This question is interesting, as there may be seasonal factors that are influencing the number of accidents. It will be interesting to see if there is a pattern to see if most accidents take place in the winter when there might be turbulent weather conditions or if seasonal factors do not hold a large stake in this data. After that is determined, the severity of the accident should be measured in the different months as well, to see if seasonal factors play a part in how many people are injured/killed. It would also be interesting to see if a larger volume of accidents in a certain month automatically leads to a larger amount of people injured/killed. Once all of this information is determined and any patterns are detected, lawmakers can then work on decreasing seasonal patterns and reducing accident-causing factors that can be controlled.


<img width="632" alt="Screenshot 2023-12-05 at 9 33 27 AM" src="https://github.com/haileytrivedi/MIST-GROUP-PROJECT-2/assets/149614680/8720f687-a5c9-4f39-add4-2398e2001117">



## Manipulations Applied

Before uploading the dataset into tableau, we limited the rows to 500 rows to cut down the amount of storage and computer power needed to run analysis on the data. For the map visualization, a manipulation and calculation was performed on the data. First, we only included the following vehicle types as they were the most common types and provided the significant data points: box truck, bus, e-bike, motorcycle, pick-up truck, sedan, station wagon/sport utility vehicle, and taxi. Additionally, we calculated the total number of people injured by adding together: 
[Number Of Persons Injured]+[Number Of Motorist Injured]+[Number Of Pedestrians Injured]+[Number Of Persons Injured]. 
	
 
 For the visualization with three charts, numerous calculations were made to create this. The same injured calculation was done as well as the sum of those killed. Numerous calculations were used to create the data regarding the contributing factor for the motor vehicle accident. In the data source tab, we counted the number of instances if the data included “Alcohol,” “Unsafe,” “Distraction,” “Too Closely,” or “Aggressive Driving.” For alcohol the code was the following: 
COUNT(IF CONTAINS([Contributing Factor Vehicle 1],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 2],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 3],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 4],"Alcohol") THEN 1 END)+COUNT(IF CONTAINS([Contributing Factor Vehicle 5],"Alcohol") THEN 1 END).


This code allowed us to sum the amount of those occurrences to segregate the data based on the contributing factor. This allowed us to see whether there was one dominating contributing factor. It also allowed us to visualize contributing factors on the same x-axis as the number of people injured/killed to see if there was a correlation. These manipulations allowed us to break out these factors based on month to also see if seasonality had an impact.


## Anyalysis and Results
