#An analysis of a policing dataset from Colchester in 2023
Data visualisation using R on the crime and weather dataset of colchester, Essex,UK

**INTRODUCTION**

We are analyzing the policing dataset from Colchester in the year 2023. Two datasets namely crime and temp2023 are analysed here under variable crime_data1 and temp_data2.Crime_data1 consists of information related to crime types, locations, latitude, longitude, street ID, street name, etc related to crime from Colchester over the year 2023. temp_data2 consists of weather details of station ID 3590 close to Colchester. So Let’s assume that the weather data is related to Colchester over the year 2023.

**DATA DESCRIPTION AND PREPROCESSING**
crime_data1 contains 6878 rows and 12 columns, temp_data2 contains 365 rows and 18 columns. The summary of the two datasets shows the details of each column to understand the nature, class, number of NA values, mean, and median if the columns contain numeric data. Crime_data1 contains numeric datatype in lat, long, and id and the rest of the columns have character class datatype. temp_data2 contains numeric datatype stationID, TemperatureCAvg, TemperatureCMax, TemperatureCMin, TdAvgC, HrAvg, WindkmhInt, WindkmhGust, PresslevHp, Precmm, TotClOct,lowClOct, SunD1h, VisKm, PreselevHp, SnowDepc and character class datatype as Date, WindkmhDir, etc. We see in temp_data2 station ID 3590 is constant and the whole report is related to one station ID i.e. 3590.

As part of data pre-processing on the crime data. We have filtered the na values. We could see the main columns have all the details except a few columns where null values were cited such as persistent_id, context id,location_subtype, and outcome_status. We have removed the column context from the dataset as contains no values and removing the column doesn’t impact the dataset. Also, we have filled the location sub_type as unknown to the null value columns.


![image](https://github.com/user-attachments/assets/486f64e8-62d1-4327-b828-770c2f37575e)
The above table shows the number of location_type and category of crime accordingly. Location BTP has a very low rate of crime when compared to Force location_type.

**EXPLORATORY DATA ANALYSIS**

![image](https://github.com/user-attachments/assets/1355a4f3-40a5-4797-b973-087d955c6383)

The above scatter plot shows the distribution of different categories of crimes in Colchester in 2023 based on the location_type named BTP and Force. Force location_type has increased crime rate when compared to BTP which maintains the crime rate at minimal.





![image](https://github.com/user-attachments/assets/36276e7f-db73-4fbb-8621-14ba1c39428a)

The above pie chart shows the rate of each crime category in Colchester for the year 2023. Interactive functions are used to show the crime and its rate based on the color to give better visualization to see the percentage for the minimal margin crimes as well. violent crime has the highest contribution of 38.28% and the least crime recorded is possession of weapons of 1.08%.

![image](https://github.com/user-attachments/assets/8ad5c126-6f81-4d73-9a13-74972fbb3277)

The above bar chart shows the top 10 street names recorded with the highest crimes in Colchester year 2023. This shows the street name on or near records the highest crime count of 495 in the year 2023.


![image](https://github.com/user-attachments/assets/5f91f15d-d008-4e33-aa90-f8ebd4f24f09)
The above graph shows the different crime categories recorded for each month. The volume of the crime is recorded by the color. Violent crime captures most of all the months. January and September record more crimes when compared to the other months.


![image](https://github.com/user-attachments/assets/af97099f-128e-45cb-8620-3a0dc1923341)

The graph shows the recorded crime in Colchester for the year 2023. The count of recorded crimes for each month is visualized here. The trend shows that during the summer and autumn seasons, the crime rates are highly recorded as the people gatherings are much sited during these months. September records the second highest of 642 crimes across Colchester as it is the start of the new academic year in universities, colleges, and schools. and January captures the highest 651 crime count as it is very evident of the new year season and celebration.







