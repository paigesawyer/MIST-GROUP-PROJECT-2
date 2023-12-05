# MIST-GROUP-PROJECT-2

## Team Name

Megan Gentles

Lindsay Kilpatrick

Aaron Phelps

Paige Sawyer

Sahana Solipuram

Hailey Trivedi



## Description of Data Set

The dataset used in this project contains information on motor vehicle collisions in New York City from 2013 to 2023, and it was last updated on December 2nd, 2023. This dataset was obtained through data.gov and specifically the catalog of various datasets (https://catalog.data.gov/dataset/motor-vehicle-collisions-crashes). It is worth noting that this dataset comes from police reports on the collisions, which are only required to be filled out if someone is injured or killed in the collision or if there is at least $1000 worth of damages. Our dataset has a variety of different data types present within it, including date and datetime in order to document when the collision occurred. There is also geographic data for latitude, latitude and zip code. Finally, we have multiple string fields for up to five contributing factors or vehicles involved in the collision and numbers to keep track of how many individuals are injured or killed both in general and broken down among cyclists, motorists and pedestrians specifically. This variety of data types and their amount allow us to take a deep dive into determining many different factors behind these collisions in the hopes of reducing the frequency and severity of them over time.



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

In conducting a comprehensive analysis of the New York City motor vehicle collision dataset spanning the years 2013 to 2023, our exploration yielded profound insights into critical factors shaping accident patterns and severity. The investigation into the geographical distribution of incidents unveiled potential hotspots within the city, underscoring the imperative for targeted interventions in specific areas to curtail the overall frequency of motor vehicle accidents. Furthermore, our scrutiny of the relationship between the types of vehicles involved in accidents and the resultant number of injuries brought to light significant considerations for the formulation of preventative legislation, identifying common vehicle types predisposed to accidents.

Our temporal analysis centered on discerning patterns in motor vehicle incidents throughout the year. Through an evaluation of monthly trends, our study sought to determine if particular months exhibited a heightened incidence of accidents and whether seasonal factors contributed to this variability. Additionally, the exploration of the correlation between the total number of accidents and resulting injuries furnished crucial insights for strategic emergency response planning and judicious resource allocation.

Our applied manipulations, including the judicious limitation of the dataset to 500 rows for optimal computational efficiency and the meticulous categorization of vehicle types and contributing factors, facilitated the creation of targeted visualizations. Utilizing Tableau, our team adeptly visualized the intricate relationships between contributing factors, vehicle types, and the number of injuries, offering a nuanced and comprehensive understanding of the dataset. These discerning analyses and visual representations serve as a robust foundation for evidence-driven policymaking and strategic interventions to alleviate the impact of motor vehicle collisions in the dynamic context of New York City.

