# Research on the Association between Location Descriptions and Specific Types of Crime

## Proposal

<img src="Overview of the project.png" width="1000px">

The study of the association between location descriptions and specific types of crime aims to understand the spatial distribution characteristics of criminal behavior. This understanding is crucial for preventing crime, formulating policing strategies, and urban planning. Numerous studies have shown that different types of criminal behavior exhibit significant spatial clustering, which is closely related to socio-economic characteristics, environmental conditions, and human activities at specific locations.
Brantingham and Brantingham (1981) proposed the Crime Pattern Theory, which posits that criminal behavior is concentrated in certain locations that typically possess features attracting criminal activities, such as commercial areas and entertainment venues. Sherman (1995) found that 50% of crimes are concentrated in 5% of locations, which are usually high-crime areas. The distribution characteristics of different types of crime vary across different locations. For example, theft and robbery are often prevalent in stores and commercial districts, while schools and residential areas may be hotspots for violent crimes and drug-related offenses. Felson and Clarke (1998) noted that location characteristics, such as accessibility and surveillance, significantly impact the type of crime that occurs.

Research on the association between location descriptions and crime types needs to consider multiple factors, such as socio-economic conditions and environmental characteristics. Existing studies in this area are still insufficient. Thus, the proposed research will aim to answer the following question:

**1.	What are the distribution characteristics of different types of crime in various locations?**
**2.	Which location descriptions are significantly associated with specific types of crime?**
**3.	How do socio-economic conditions and environmental characteristics affect the spatial distribution of criminal behavior?**



This study aims to systematically analyze the association between location descriptions and specific types of crime, using spatiotemporal data to identify high-risk locations and crime types, thereby providing a basis for targeted crime prevention strategies.


In addition, this study will choose Chicago as the representative city. Chicago is a large, diverse city with a wide range of socio-economic conditions, environmental settings, and urban layouts, making it an ideal microcosm for studying crime patterns that can be extrapolated to other urban areas. The city has a long history of detailed crime data collection, providing a rich temporal dataset essential for analyzing trends and patterns over time. Known for its significant crime rates, Chicago serves as a critical area of study for understanding the underlying factors and developing effective crime prevention strategies. Furthermore, the city experiences a broad spectrum of crime types, from violent crimes to property crimes, allowing for a comprehensive analysis of how different crimes correlate with specific location descriptions.


## Data
This dataset contains records of reported crimes (excluding murders, which are documented for each individual victim) that have taken place in the City of Chicago from 2001 to the present. The data is sourced from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. You can find the data via the [link](bridgeport_crime_by_longitude_latitude_location_20240803.csv).

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



## KNIME Workflow
This workflow demonstrates a complete process of data processing and geospatial visualization using KNIME. First, the CSV Reader node is used to load data from a CSV file, and the Table View node checks if the data is loaded correctly. Next, the Column Filter node selects the necessary columns, filtering out the unneeded data. Then, the Lat/Lon to Geometry node converts latitude and longitude data into a geometry format for further processing. Subsequently, the Nominal Value Row Filter node removes rows with missing data to ensure data integrity. Finally, the Geospatial View node performs geospatial visualization, presenting the processed data visually. This workflow effectively transitions data from the raw CSV file to the final geospatial visualization with clear and logical steps.

<img src="Workflow Display.png" width="1000px">

The sample result is shown here.



<img src="Sample view of the result.png" width="1000px">


You can download the KNIME Workflow [here](https://github.com/Rising-Stars-by-Sunshine/SDL-workflow-tutorial/blob/be67a8d02e667f30e984d17d293ce7bb19702c1a/KNIME_project.knwf). You can import the workflow to KNIME in your computer and replicate the workflow easily.

## Reference
Brantingham, P. L., & Brantingham, P. J. (1981). Environmental Criminology. Sage Publications.

Sherman, L. W. (1995). Hot Spots of Crime and Criminal Careers: A Randomized Controlled Trial. Crime and Place, 4(1), 35-52.

Felson, M., & Clarke, R. V. (1998). Opportunity Makes the Thief: Practical Theory for Crime Prevention. Home Office, Research, Development and Statistics Directorate.

}
```
