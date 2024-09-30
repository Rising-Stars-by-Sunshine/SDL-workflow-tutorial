# Research on the Association between Location Descriptions and Specific Types of Crime
Mentee: Wanlin Deng, Duke Kunshan University, Political Economy/Economics

Mentors:   
Prof. Luyao Zhang, Duke Kunshan University 

Prof. Xiao Huang, Emory University

## SPATIAL DATA LAB (SDL) INTERNSHIP PROGRAM

The Spatial Data Lab (SDL) internship program is designed to provide academic learning experience for high school, undergraduate and graduate students. It offers tailored professional training based on a student’s academic or career interests. This internship will provide hands-on experience in utilizing open-source tools, workflow technology, geospatial data, spatial modeling, and their applications across different fields. An internship gives a student the opportunity to experience the entire life-cycle of academic research, gain hands-on experience in cutting-edge technologies, explore career directions, develop technical skills as well as leadership abilities. (Link to the program:Link: https://sdl.gis.harvard.edu/)



## Overview of the Project



<div style="text-align: center;">
    <img src="Pictures/Overview of the project.png" width="1000px">
    <p><em>Figure 1: Workflow of this project.</em></p>
</div>



The study of the association between location descriptions and specific types of crime aims to understand the spatial distribution characteristics of criminal behavior. This understanding is crucial for preventing crime, formulating policing strategies, and urban planning. Numerous studies have shown that different types of criminal behavior exhibit significant spatial clustering [[1]](#footnote1) , which is closely related to socio-economic characteristics[[2]](#footnote2), environmental conditions [[3]](#footnote3) , and human activities [[4]](#footnote4) at specific locations.
Brantingham and Brantingham (1981) proposed the Crime Pattern Theory, which posits that criminal behavior is concentrated in certain locations that typically possess features attracting criminal activities, such as commercial areas and entertainment venues. Sherman (1995) found that 50% of crimes are concentrated in 5% of locations, which are usually high-crime areas. The distribution characteristics of different types of crime vary across different locations. For example, theft and robbery are often prevalent in stores and commercial districts, while schools and residential areas may be hotspots for violent crimes and drug-related offenses. Felson and Clarke (1998) noted that location characteristics, such as accessibility and surveillance, significantly impact the type of crime that occurs.

Research on the association between location descriptions and crime types needs to consider multiple factors, such as socio-economic conditions and environmental characteristics. Existing studies in this area are still insufficient. Thus, the proposed research will aim to answer the following question:

**1.	What are the distribution characteristics of different types of crime in various locations?**

**2.	Which location descriptions are significantly associated with specific types of crime?**

**3.	How do socio-economic conditions and environmental characteristics affect the spatial distribution of criminal behavior?**



This study aims to systematically analyze the association between location descriptions [[5]](#footnote5) and specific types of crime, using spatiotemporal data [[6]](#footnote6) to identify high-risk locations and crime types, thereby providing a basis for targeted crime prevention strategies.


In addition, this study will choose Chicago as the representative city. Chicago is a large, diverse city with a wide range of socio-economic conditions, environmental settings, and urban layouts, making it an ideal microcosm for studying crime patterns that can be extrapolated to other urban areas. The city has a long history of detailed crime data collection, providing a rich temporal dataset essential for analyzing trends and patterns over time. Known for its significant crime rates, Chicago serves as a critical area of study for understanding the underlying factors and developing effective crime prevention strategies. Furthermore, the city experiences a broad spectrum of crime types, from violent crimes to property crimes, allowing for a comprehensive analysis of how different crimes correlate with specific location descriptions.


## Data
This dataset contains records of reported crimes (excluding murders, which are documented for each individual victim) that have taken place in the City of Chicago from 2001 to the present. The data is sourced from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. You can find the data in the [Github](bridgeport_crime_by_longitude_latitude_location_20240803.csv) or via the [original website](https://data.cityofchicago.org/Public-Safety/bridgeport-crime-by-longitude-latitude-location/srg9-gsb8/about_data).

### Preview of the Data
| ID  | Case Number | Date | Block | IUCR|Primary Type| Description |
| ----| ------------| -----|-------|-----|-----|-----|
| 13243446  | JG462969  | 10/12/2023 01:50:00 PM| 007XX W 31ST ST|	860	|THEFT	|RETAIL THEFT|


|Location Description |Arrest	|Domestic |Beat	|Ward| FBI Code |X Coordinate |Y Coordinate|
|-------|-----|-----|-----|-----|-----|-----|-----|
|	SMALL RETAIL STORE| FALSE |FALSE|	915	|11	|6	|1171721	|1884329	|

|Year|Updated On	| Latitude| Longitude| Location|
|-----|-----|-----|-----|-----|
|2023	|10/20/2023 03:45:23 PM| 41.83805721|	-87.64537032	|(41.838057207, -87.645370318)|



## KNIME Workflow and Configuration
Figure2 demonstrates a complete workflow of data processing and geospatial visualization using KNIME. First, the CSV Reader node is used to load data from a CSV file, and the Table View node checks if the data is loaded correctly. Next, the Column Filter node selects the necessary columns, filtering out the unneeded data. Then, the Lat/Lon to Geometry node converts latitude and longitude data into a geometry format for further processing. Subsequently, the Nominal Value Row Filter node removes rows with missing data to ensure data integrity. Finally, the Geospatial View node performs geospatial visualization, presenting the processed data visually. This workflow effectively transitions data from the raw CSV file to the final geospatial visualization with clear and logical steps. You can download the KNIME Workflow [in the Github](https://github.com/Rising-Stars-by-Sunshine/SDL-workflow-tutorial/blob/be67a8d02e667f30e984d17d293ce7bb19702c1a/KNIME_project.knwf). You can import the workflow to KNIME in your computer and replicate the workflow easily. Or you can go to the [KNIME hub](https://hub.knime.com/wanlin_deng/spaces/Public/KNIME_project~SfmkAWdjz4a2YP59/current-state) and drag the workflow to your software directly.


<div style="text-align: center;">
    <img src="Pictures/Workflow Display.png" width="800px">
    <p><em>Figure 2: Workflow display showing the sequence of steps in the project.</em></p>
</div>

First, you need to modify the data path to ensure that the file can be properly loaded. 

<div style="text-align: center;">
    <img src="Pictures/CSV reader configuration.png" width="800px">
    <p><em>Figure 3: CSV reader configuration.</em></p>
</div>

Then, filter out the useful columns, including ID, Date, Block, Primary Type, Description, and Location Description. 

<div style="text-align: center;">
    <img src="Pictures/Column filter configuration.png" width="800px">
    <p><em>Figure 4: Column filter configuration.</em></p>
</div>


Next, in the row filter, select the "Location" column and choose "Exclude" in the Missing value handling to remove crime records without geographic location information. 

<div style="text-align: center;">
    <img src="Pictures/Row filter configuration.png" width="800px">
    <p><em>Figure 5: Row filter configuration.</em></p>
</div>

Finally, configure the necessary information to be displayed on the map in the "Geospatial view" node.

<div style="text-align: center;">
    <img src="Pictures/Geospatial view configuration.png" width="800px">
    <p><em>Figure 6: Row filter configuration.</em></p>
</div>



The sample result is shown in the figure7.

<div style="text-align: center;">
    <img src="Pictures/Sample view of the result.png" width="800px">
    <p><em>Figure 7: Sample view of the result.</em></p>
</div>






## Reference
Brantingham, P. L., & Brantingham, P. J. (1981). Environmental Criminology. Sage Publications.

Sherman, L. W. (1995). Hot Spots of Crime and Criminal Careers: A Randomized Controlled Trial. Crime and Place, 4(1), 35-52.

Felson, M., & Clarke, R. V. (1998). Opportunity Makes the Thief: Practical Theory for Crime Prevention. Home Office, Research, Development and Statistics Directorate.

## Footnote

1. <a name="footnote1"></a> Spatial Clustering: Refers to the phenomenon where similar types of criminal behavior are concentrated in specific geographic areas. This often indicates that certain locations, due to their environmental or socio-economic characteristics, are more prone to specific types of crime.
2. <a name="footnote2"></a> Socio-economic Characteristics: Includes social and economic factors such as income levels, employment status, and education levels. These factors are often correlated with crime rates. For example, economically disadvantaged areas may be more susceptible to property crimes.
3. <a name="footnote3"></a> Environmental Conditions: Refers to the physical environment and infrastructure of a specific location, such as lighting, road layout, and public transportation facilities. These conditions can influence the crime rate in an area. For instance, poorly lit areas may be more prone to criminal activity.
4. <a name="footnote4"></a> Human Activities: Encompasses various activities that people engage in at specific locations, such as shopping, entertainment, or attending school. These activities can impact the types and frequency of crimes that occur in an area.
5. <a name="footnote5"></a> Location Descriptions: Refers to the characteristics or features of a specific location, which may include its function (e.g., stores, schools, residential areas) or attributes (e.g., remote, easily accessible). Different location descriptions may be associated with different types of crime.
6. <a name="footnote6"></a> Geospatial Data: Contains information about geographical locations, used to analyze the spatial distribution and correlation of criminal behavior. This type of data typically includes coordinates, addresses, and area names.

