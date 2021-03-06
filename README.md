# DataProject_ElwhaRiver

**Changes on the Elwha River During Dam Removal**


Environmental Data Analytics Course Project Focused on the Elwha River


## Summary

This repository stores relevant data sets, and rmarkdown code for analysis of water discharge and sediment loads on the Elwha River. Analysis focuses on the time frame during and after the removal of Glines Canyon Dam and the Elwha Dam, both on the Elwha River, Washington. 

The dataset begins when the removal project begins, September 15, 2011. The Glines Canyon Dam was removed not long after, and the project officially ended on August 26, 2014, but the data was collected until September 30, 2016. Data was recorded by the USGS gage station with identification number- 12046260, which can be found downstream of the old dams sites at the diversion near Port Angeles, Washington.

An understanding of changes on the Elwha River during and following the dam removal process can be understood from analysis on daily water discharge, and parameters surrounding sediment concentration, bedload, size of sediment, and sediment discharge. Looking at changes of these parameters over time in accordance with the time stamps of the project can help explain how long it takes a river to reach a new stability of discharge and sediment discharge following dam removal. The in depth analysis will focus on potential changes in water discharge and total sediment discharge during and after the dam removal process.

## Database Information

Data was collected daily at the USGS gaging station with identification number 12046260, located on the Elwha River at the diversion near Port Angeles, Washington. Data was published February 7, 2020 and accessed April 20, 2020. The date range of the data is 2011-09-15 to 2016-09-30. The dataset is part of a larger study that created a 5 year sediment budget and morphodynamic analysis of the Elwha River following the two dam removals.

Analysis was performed by a graduate student at the Nicholas School of the Environment, Duke University.


## Investigators

**U.S. Geological Survey**

Dataset Source: Data in support of 5-year sediment budget and morphodynamic analysis of Elwha River following dam removals, Daily sediment loads during and after dam removal in the Elwha River, Washington, 2011 to 2016, U.S. Geological Survey

<https://doi.org/10.5066/F7PG1QWC>



*Contributers: Ritchie, A.C., Curran, C.A., Magirl, C.S., Bountry, J.A., Hilldale, R.C., Randle, T.J., and Duda, J.J.

*Point of Contact: Christopher S Magirl, U.S. Geological Survey, Arizona Water Science Center

*Originator: Christopher S Magirl, Christopher A Curran, Robert C Hilldale

*Metadata Contact :Christopher S Magirl, U.S. Geological Survey, Arizona Water Science Center

*Publisher: U.S Geological Survey

*Data Distributor: U.S. Geological Survey- SienceBase

*Publication Date: February 7, 2018

**Data Analysis:**

*Kathleen Mason, Duke University, Nicholas School of the Environemnt, Master of Environmental Maangement Candidate, kfm20@duke.edu

*Analyzed April 2020 as part of a course project fro ENV872L, Environmental Data Analytics, by Professor Kateri Salk-Gunderson

## Keywords

Elwha River, Elwha Dam, Glines Canyon Dam, Port Angeles, Washington, dam removal, sediment loads, discharge, river, suspended sediment, sediment loads, fine-grained particles, sand, bedload, post dam removal, river morphology, river flow, USGS, sediment budget


## Folder structure, file formats, and naming conventions 

**Folder Structure:**
*Code-R markdown code for data wrangling, data exploration/analysis, and data visualization

*Output-This contains any .jpg or .png exported files of graphs and any .pdf documents of maps, as well as.

*Processed-Exported .csv files of wrangled datasets, so particular formatted datasets can be accessed again or shared.

*Raw- Original .txt file of the USGS data, which is also saved as a .csv file for use in R.


**Naming Convention:**

Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated, all files in this folder include USGS, or the U.S. Geological Survey

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data or outputs

**stage**refers to the stage in data management pipelines (raw, wrangled, or processed)

**format** is a non-proprietary file format (.csv, .txt, .pdf, .png, .jpg, .xlsx)



## Metadata

**USGS_ElwhaDischarge_raw.csv**

Column name | Data Description | Class | Associated Units
--------|-----|--------|-------
Day|Date of daily recording|Date|
Daily Discharge (m3/s)|Daily water discharge from the river|numeric| m3/s
Daily SSC (mg/L) | Daily suspended sediment concentration| numeric| mg/L
Upper SSC Bound (+1SD)| Suspended sediment, one standard deviation, upper bound| numeric| mg/L
Lower SSC Bound (+1SD)| Suspended sediment, one standard deviation, lower bound|numeric| mg/L
Ave fraction fines (based on two turbidimeters)| Average fraction of fine grained sediment (silts and clay) in suspension|numeric|
Daily Suspended sediment loads (tonnes)| Daily total suspended sediment load|numeric|tonnes
Daily SS loads of fines (tonnes)|Daily suspended fine grained sediment load |numeric|tonnes
Daily SS loads of sand (tonnes)| Daily suspended sand sediment load|numeric|tonnes
Remarks|General notes added|character|
Daily total gauged >2 mm bedload (tonnes)|Gauged bedload for particles greater than 2mm|numeric|tonnes
Daily total gauged >2-16 mm particles (tonnes)|Gauged bedload for particles between 2-16 mm|numeric|tonnes
Daily total gauged >16 mm particles (tonnes)|Gauged bedload for particles > 16 mm|numeric|tonnes
Estimated daily ungauged bedload (tonnes)|Estimated bedload for particles <2mm |numeric| tonnes
Total sediment discharge (tonnes)|Total daily sediment discharge|numeric|tonnes
Release period|Stage of dam removal|character|
Project year| Year of sampling project, extending from 1-5 years|character|year


**USGS_ElwhaRiver_processed.csv**

Column name | Data Description | Class | Associated Units
--------|-----|--------|-------
Date|Date of daily recording|Date|YYYY-MM-DD
DailyDischarge|Daily water discharge from the river|numeric| m3/s
DailySSC | Daily suspended sediment concentration| numeric| mg/L
DailySuspendedSediment| Daily total suspended sediment load|numeric|tonnes
DailySSfines|Daily suspended fine grained sediment load |numeric|tonnes
DailySSsand| Daily suspended sand sediment load|numeric|tonnes
TotalSedimentDischarge|Total daily sediment discharge|numeric|tonnes
Project year| Year of sampling project, extending from 1-5 years|character|year


**USGS_ElwhaRiverDischarge_TimeStamped_processed.csv**

This have the same parameters as the above datasets but it has an additional column labeled "TimeStamp". This character column distinguishes "during" data that follows dates during the dam removal process, all dates from September 15, 2011 to August 26, 2014. The "after" data follows dates after the dam removal process was complete, August 27, 2014 to September 30, 2016. 


**USGS_ElwhaRiverDischarge_During_processed.csv**

**USGS_ElwhaRiverDischarge_After_processed.csv**

This has the same parameters as the aboce datasets, but instead it is divided into two different datasets based on teh Time Stamp column. The "during" dataset file includes data with dates from September 15, 2011 to August 26, 2014. The "after" dataset includes data with dates after the dam removal process was complete, August 27, 2014 to September 30, 2016. 


## Scripts and code

**DataWrangling.Rmd**

This includes the steps required to create a tidy dataset with the variables most necessary for the analysis, in their own columns, and observations in their own cells, with no blank cells. These steps are essential for proper analysis and visualization to be performed. Class of columns are specified, and column headers edited. 

**DataExploration.Rmd**

Exploration of the dataset to see if there are any outliers, missing data, or out of range data. I test out multiple plots to see what data is the best displayed, and what sort of analyses are necessary moving forward. Initial visualizations are performed to find trends, outliers, and potential relationships. Edited datasets are saved as processed files.

**DataVisualization.Rmd**

Lineplots are created to show trends of parameters over time. Research into the dam removal process on the Elwha River provides dates to show time stamps, which are fitted into the plots. The sampling began at the start of the dam removal process, and one dam was removed in year 2 of sampling. The dam removal process on the Elwha River finished in year 4 of sampling, and data continued to be collected for 2 more years following. Trends most interesting that are analyzed include water discharge compared with total sediment discharge and daily suspoended sediment. Daily suspended solids of fine particles and sand are also compared too see the make up of the sand flowing downstream. 

**Mason_ENV872_ProjectFinal.Rmd**

This includes the final write up for my class report, it includes relevant information about the data set, the perfomred explanatory analysis with figures, research questions and rationale, and results represented throught a writeup and visualizations. This same file is also stored as a .tex, .log, and .pdf.


## Quality assurance/quality control

*Sampling occured under the U.S Geological Survey, a prestigious agency with years of expertise in these fields, which make the protocols for sampling credible.

*All values are checked to see if they are within an expected range of data.

*Remarks, or notes, are made on data points that may have followed a different protocol. Some data points are marked with "estimated."

*Boxplots and visualization techniques are used to discover any outliers within data, and these are flagged accordingly. 

*Data wrangling, exploration, and visualization steps within R are properly annotated for reproducible analysis.

*Naming conventions are used for reproducible files and datasets. 

 