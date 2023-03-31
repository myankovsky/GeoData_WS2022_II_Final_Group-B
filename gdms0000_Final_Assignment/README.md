# EE_3.07 Geodata Management Systems WS2022/23 - <br> Final Assignment

## 1. Warming Stripes 

The task involves creating a plot that visually represents the annual temperature data of 13 weather stations in NRW, Germany in a warming stripes format. This requires the use of various Python libraries and techniques such as Pandas, geopandas, seaborn, and data retrieval techniques like FTP.

To accomplish this task, we need to start with the first sub-task, which involves selecting 13 weather stations in NRW that are still active and started before 1950. This requires reading the station description file from the historical KL data collection using Pandas. We can use the information in this file to filter out the stations that meet our criteria. We need to ensure that the stations are still active so that we can retrieve the most recent data. Additionally, we need to make sure that the stations have been operational since before 1950, so we have enough data to analyze.

The second sub-task involves using geopandas to create a geopackage layer with the 13 stations and loading it into QGIS to create a map with NRW WMS service as the background map. This will enable us to locate the stations and see their relative positions on a map. The geopackage layer we create will contain the necessary information about the stations such as their IDs and names. We can use this information to label the stations on the map and make it easier to identify each station.

The third sub-task involves downloading the annual temperature data for the selected stations automatically from the KL data collection using FTP.. This involves writing a Python script that automatically downloads the necessary data based on the station IDs from the station info dataframe. This is an essential step as we need to collect the annual temperature data for the selected stations to analyze and plot them in a warming stripes format.

The fourth and final sub-task requires using the temperature data from the selected stations to create a warming stripes plot. We can use seaborn, a Python data visualization library, to create the plot. The warming stripes plot visually represents the annual temperature changes at each station over time. The plot displays the temperature data as a series of colored stripes, with each stripe representing a year. The color of each stripe is based on the temperature difference from a reference temperature, with red indicating above-average temperatures, and blue indicating below-average temperatures.

We can copy the relevant code from the notebook [gdms0155_DWD_NRW_5_Warming_Stripes/gdms155_DWD_NRW_5_Warming_Stripes.ipynb] and modify it to suit our needs. This involves adjusting the code to include the 13 selected stations and plotting the annual temperature data from 1950 to 2022. The resulting plot will provide insights into the annual temperature changes at each station, making it easier to compare and contrast the temperature trends.

In summary, the task involves analyzing and visualizing annual temperature changes at 13 weather stations in NRW, Germany, using warming stripes plots. This requires selecting the appropriate stations, creating a geopackage layer, retrieving the annual temperature data, and using Python libraries such as seaborn to create the plots. This task is essential for understanding the impact of global warming on our climate and for developing strategies to mitigate its effects.

## 2. Digitization: Burial Mounds in Uedemer Hochwald (20 Points)

South west of the village Marienbaum, which belongs to the Xanten municipality in Germany, lies the Uedemer Hochwald forest. This forest is home to many burial mounds, known as "Hügelgräber" in German, which were constructed by our ancestors during the Hallstatt period, a Celtic culture that existed between 850 and 450 BCE. Some of these burial mounds are indicated as grey dots on the map section shown above.

For Task 2.1, we were required to georeference the picture of the map above. We started with the QGIS project gdms0000_Burial_Mounds_Uedem_V001.qgz in the assignment folder and used the QGIS Georeferencer tool. We combined this with the layer DTK10, which is the NRW topographic map in a 1:10000 scale, already imported from the NRW WMS server and added in the QGIS project. To complete this task, we used crossing forest trails, crossroads, road junctions, and other features we could identify on DTK10 as landmarks (also known as ground control points, GCP) with known coordinates that could be read from the QGIS map canvas. We used EPSG:25832 and added the georeferenced map to the QGIS project.

For Task 2.2, we created a hillshade model from the DTM layer and plotted our georeferenced map partly transparent on top of the hillshade model. By comparing the two, we observed that the burial mounds on the georeferenced map were quite visible.

In Task 2.3, we were asked to use the DTM (not the hillshade model) to measure the typical mound heights relative to their direct environment or neighborhood, rather than the absolute height above sea level. We found that the typical elevation of the burial mounds in the landscape was XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Task 2.4 required us to study the hillshade model in the direction of East-North-East of the burial mounds area and search for weakly visible rectangular structures that were not paths. We observed some patterns that seemed to fit this description, and we had a few guesses about their origin. We chose at least one of the structures, digitized it with a polygon, and saved it as a geopackage.

## 3. OpenHygrisC Nitrate Data: Create a Movie with the QGIS Temporal Controller Connected to PostgreSQL / PostGIS (20 Points)

Data Preparation:
To begin, the OpenHygrisC groundwater quality data were downloaded and engineered. Station information and measurement data were loaded into the geodatabase, which is stored in PostgreSQL/PostGIS. This data was utilized to create a catalog of substances, which is also stored in the database.

Database Optimization:
In the course of the project, several database optimization techniques were employed to improve data retrieval performance. These included creating several indexes, which are used to quickly find data that matches a certain set of criteria. Additionally, views were created in the database, which are stored queries that generally join and project relations. These views are used to simplify and streamline data retrieval.

System Execution:
To execute the OpenHypE system, we began by accessing the OpenHyPE git repo, where the relevant code is stored. The code was read and executed to get the system up and running. The QGIS Temporal Controller was utilized to produce a video of Nitrate concentration from the earliest available Nitrate measurement in the early 1960s up to the latest measurement.

Conclusion:
Overall, the OpenHypE system is an important tool for analyzing groundwater quality data using spatio-temporal data analysis techniques. The system consists of OpenHygrisC data, which includes station locations, measurement data, and a catalog of substances stored in PostgreSQL/PostGIS. Database optimization techniques, including creating indexes and views, were employed to improve data retrieval performance. The QGIS Temporal Controller was utilized to produce a video of Nitrate concentration from the earliest available Nitrate measurement to the latest measurement.



## 4. FREE EXERCISE (20 Points)

We tried to make an analysis of the public transportation in some german cities and import this information to qgis to see where less people use public transport. TO make this task we found the information about major german cities population, public transort usage (number of people carried by public transport inside a city) and geodata. THen we calculated the number that indicates the relation between population and public transport usage (Number of people used public transort per day divided by population of the city (numpop)). Then we converted our csv table to geopackage layer and projected the information on the map in qgis.

## 5. Produce a Video and Explain your Methods and Achievements. 

Done. You can find a link to the video here: 


