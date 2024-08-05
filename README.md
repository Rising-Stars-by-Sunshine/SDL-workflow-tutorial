# Research on the Association between Location Descriptions and Specific Types of Crime

## Proposal

The study of the association between location descriptions and specific types of crime aims to understand the spatial distribution characteristics of criminal behavior. This understanding is crucial for preventing crime, formulating policing strategies, and urban planning. Numerous studies have shown that different types of criminal behavior exhibit significant spatial clustering, which is closely related to socio-economic characteristics, environmental conditions, and human activities at specific locations.
Brantingham and Brantingham (1981) proposed the Crime Pattern Theory, which posits that criminal behavior is concentrated in certain locations that typically possess features attracting criminal activities, such as commercial areas and entertainment venues. Sherman (1995) found that 50% of crimes are concentrated in 5% of locations, which are usually high-crime areas. The distribution characteristics of different types of crime vary across different locations. For example, theft and robbery are often prevalent in stores and commercial districts, while schools and residential areas may be hotspots for violent crimes and drug-related offenses. Felson and Clarke (1998) noted that location characteristics, such as accessibility and surveillance, significantly impact the type of crime that occurs.

Research on the association between location descriptions and crime types needs to consider multiple factors, such as socio-economic conditions and environmental characteristics. Existing studies in this area are still insufficient. Thus, the proposed research will aim to answer the following question:

1.	What are the distribution characteristics of different types of crime in various locations?
2.	Which location descriptions are significantly associated with specific types of crime?
3.	How do socio-economic conditions and environmental characteristics affect the spatial distribution of criminal behavior?



This study aims to systematically analyze the association between location descriptions and specific types of crime, using spatiotemporal data to identify high-risk locations and crime types, thereby providing a basis for targeted crime prevention strategies.


In addition, this study will choose Chicago as the representative city. Chicago is a large, diverse city with a wide range of socio-economic conditions, environmental settings, and urban layouts, making it an ideal microcosm for studying crime patterns that can be extrapolated to other urban areas. The city has a long history of detailed crime data collection, providing a rich temporal dataset essential for analyzing trends and patterns over time. Known for its significant crime rates, Chicago serves as a critical area of study for understanding the underlying factors and developing effective crime prevention strategies. Furthermore, the city experiences a broad spectrum of crime types, from violent crimes to property crimes, allowing for a comprehensive analysis of how different crimes correlate with specific location descriptions.


## Data
This dataset contains records of reported crimes (excluding murders, which are documented for each individual victim) that have taken place in the City of Chicago from 2001 to the present. The data is sourced from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system.

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

<img src="Workflow display" width="1000px">

The sample result is shown here.



<img src="Sample view of the result.png" width="1000px">


You can download the KNIME Workflow [here](https://github.com/Rising-Stars-by-Sunshine/SDL-workflow-tutorial/blob/c560255739a1d2194e7a2793e63fed10a86c8796/Sample%20view%20of%20the%20result.png). You can import the workflow to KNIME in your computer and replicate the workflow easily.

## Reference
Brantingham, P. L., & Brantingham, P. J. (1981). Environmental Criminology. Sage Publications.

Sherman, L. W. (1995). Hot Spots of Crime and Criminal Careers: A Randomized Controlled Trial. Crime and Place, 4(1), 35-52.

Felson, M., & Clarke, R. V. (1998). Opportunity Makes the Thief: Practical Theory for Crime Prevention. Home Office, Research, Development and Statistics Directorate.

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Amine, Amrani. 2020. “Q-Learning Algorithm: From Explanation to Implementation.” Medium. December 19, 2020. https://towardsdatascience.com/q-learning-algorithm-from-explanation-to-implementation-cdbeda2ea187.

“Backward Induction.” 2019. Investopedia. 2019. https://www.investopedia.com/terms/b/backward-induction.asp.

Govindan, Srihari, and Robert Wilson. 2009. “On Forward Induction.” Econometrica 77 (1): 1–28. https://www.jstor.org/stable/40056520.

Haiyan, Li. 2018. “Dynamic Trust Game Model between Venture Capitalists and Entrepreneurs Based on Reinforcement Learning Theory.” Cluster Computing 22 (S3): 5893–5904. https://doi.org/10.1007/s10586-017-1666-x.

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

Liu, Bingjie, and Lewen Wei. 2022. “Unintended Effects of Open Data Policy in Online Behavioral Research: An Experimental Investigation of Participants’ Privacy Concerns and Research Validity.” Computers in Human Behavior, October, 107537. https://doi.org/10.1016/j.chb.2022.107537.

“Pareto Efficiency - an Overview | ScienceDirect Topics.” n.d. Www.sciencedirect.com. https://www.sciencedirect.com/topics/economics-econometrics-and-finance/pareto-efficiency.

Pettinger, Tejvan. 2019. “Social Efficiency.” Economics Help. September 17, 2019. https://www.economicshelp.org/blog/2393/economics/social-efficiency/.

“Strategy (Game Theory).” n.d. Encyclopedia.pub. Accessed May 10, 2023. https://encyclopedia.pub/entry/36857.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Govindan, Srihari, and Robert Wilson},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2018},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```
```
@article{
  title={Dynamic Trust Game Model between Venture Capitalists and Entrepreneurs Based on Reinforcement Learning Theory},
  author={Li,Haiyan},
  journal={Computers in Human Behavior},
  volume={October},
  number={107537},
  year={2022}
}
```
```
@article{
  title={Unintended Effects of Open Data Policy in Online Behavioral Research: An Experimental Investigation of Participants’ Privacy Concerns and Research Validity},
  author={Liu, Bingjie, and Wei Lewen},
  journal={Cluster Computing},
  volume={22},
  number={S3},
  pages={5893–5904},
  year={2022}
}
```
```
@article{
  title={Q-Learning Algorithm: From Explanation to Implementation},
  author={Amine, Amrani},
  journal={Medium},
  year={2020},
  url={https://towardsdatascience.com/q-learning-algorithm-from-explanation-to-implementation-cdbeda2ea187}
}
```
```
@article{
  title={Backward Induction},
  journal={Medium},
  year={2019},
  url={https://www.investopedia.com/terms/b/backward-induction.asp}
}
```
```
@article{
  title={Pareto Efficiency - an Overview | ScienceDirect Topics.},
  author={Pettinger, Tejvan},
  year={2019},
  journal={Economics Help.},
  url={https://www.economicshelp.org/blog/2393/economics/social-efficiency/](https://www.economicshelp.org/blog/2393/economics/social-efficiency/}
}
```
```
@article{
  title={Pareto Efficiency - an Overview | ScienceDirect Topics.},
  url={https://www.economicshelp.org/blog/2393/economics/social-efficiency/}
}
```
```
@article{
  title={On Forward Induction},
  journal={Econometrica},
  year={2009},
  pages={1--28},
  url={https://towardsdatascience.com/q-learning-algorithm-from-explanation-to-implementation-cdbeda2ea187](https://www.investopedia.com/terms/b/backward-induction.asp)](https://www.jstor.org/stable/40056520}
}
```
