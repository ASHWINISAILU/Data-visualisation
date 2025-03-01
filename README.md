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


![image](https://github.com/user-attachments/assets/818bf439-562e-425f-9c24-a782ced4275f)

The above interactive dot plot shows the distribution of different categories of crime over high-crime streets over the year 2023. This gives a details look at each crime over different months in high-crime streets. majority of the crimes captured are due to violence. When u want to zoom in to look out on the detailed crime time, it gives more visibility.



![image](https://github.com/user-attachments/assets/d9e5d09e-3f01-414a-aa3a-20ae1b0318ad)

The data on the crime are visualized through the map. based on the latitude and longitude we have marked the different categories of crime recorded in each area in Colchester. This helps to explore more high and low crime areas, planning on people’s safety. Areas to increase policing activities can also be found out easily. At each cluster point, we can zoom in and find out at street level the category of crime recorded over the areas as well. This gives us a wider picture of crime happenings in Colchester in 2023 over a map for better understanding.


![image](https://github.com/user-attachments/assets/88b947ed-04b4-4465-999a-10d5369a03d6)
The above box plot shows the boxplot for a column with numeric data type in the dataset. Since this is related data, there seems to be not much changes in the data range and the outliers are also very minimal.

Since the data is date-based information, we trying to format it from DD-MM-YYYY to the new column Month with format MM for further analysis.

![image](https://github.com/user-attachments/assets/a93510dd-391c-46e5-b6b6-18f6efbdfa36)
The above graph show the trend in temperature for the year 2023. January and December have recorded very low temperatures. and temperature has risen at its highest during June, July, August, and September months.


![image](https://github.com/user-attachments/assets/46def550-57cc-4b70-b167-d61d157d28b9)
The above line plot gives a clear picture of weather trends recorded in station ID 3590 near Colchester. Premium: This shows the total rainfall recorded at the weather station ID 3590 mm. The rainfall was high during July, and August and peaked in October months. SunD1h: Represent the duration of sunshine recorded at the weather( in hours). The sunlight recorded seems to be on the same baseline, there wasn’t much change in the sunshine recorded. VisKm: Represent the visibility recorded at the weather station( in km). The visibility factor of the weather affects the many factors in crime categories. In Colchester SnowDepcm: This shows the snow depth recorded at the weather station measured in centimeters (cm). There is not much variation recorded over the year 2023.

![image](https://github.com/user-attachments/assets/b4e6e53a-6cf7-4e5b-a329-32563ff66008)

The correlation heat map shows the relationship between each variable (columns). We can see a positive correlation with TotClOct and HrAvg, Viskm and temperature, etc. It shows that temperature, visibility, and sunlight range are positively correlated.Humidity(HrAvg) is more related to rainfall(Precmm) and cloudiness(TotClOct)etc. sunlight, humidity, and temperature are negatively correlated. Zero correlation can be seen in speed, humidity, visibility, etc. The correlation map shows how the two scales are related to each other affecting the climate.


![image](https://github.com/user-attachments/assets/4fca3b1a-0fd7-4dc7-918b-95d72b2d7e8f)
This time series shows the trend of weather and crime in Colchester for the year 2023. We are considering the top 5 categories of crime from crime_data1 and visibility and average temperature is considered from the temp_data2 file. We see the violent crimes category records the highest in the crime category. When it comes to trends visibility and temperature averages are more related. When visibility is lower in winter and higher in summer. While temperatures tend to be lower in winter and higher in summer. The visibility keeps fluctuating while the temperature keeps a moderate trend. During September anti social behavior and violent crimes are high. We can see the crime rates in December and January tend to be higher and temperature seems to be low. Similarly, in June and July, we can see the crime rates increasing again and the temperature also increasing.

This clearly shows how temperature and visibility impact the crime rates in Colchester. When the visibility and temperature are low, the crime rate tends to increase. Also during summer when the temperature is high, people become aggressive, and again crime rate seems to increase.



![image](https://github.com/user-attachments/assets/95f08e54-9803-46e6-9a45-be21edf26a56)
The smoothing technique has been implemented on the time series. The random walk method has been used to reduce fluctuations and noise in the data. The average neighboring data points are used to replace the existing data points over repeated iterations. The time series graph clearly shows a clear trend of the crimes, temperature, and visibility over the months. The random walk technique was more effective than the Loess method and moving average smoothing method on this data.


**Conclusion:**

The crime and weather data of Colchester for the year 2023 have been analyzed. There are very helpful insights for policing the Colchester areas. The categorical crime rates across Colchester are impacted by the weather. When the temperature is extreme such as too low in December and January, the visibility is also low which influences to have more crime rates across Colchester.In September and October when the rainfall increases, we can see the crime rates increasing. During summer, months like June and July see high temperatures which make it more prone for people to hang out so violent crimes, anti-social behavior, and shoplifting crimes tend to be spotted in increasing trends. So more patrols and policing have been in place during January, June, July, September, October, and December.

