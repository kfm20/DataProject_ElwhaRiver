# DataProject_ElwhaRiver
Environmental Data Analytics Course Project Focused on the Elwha River


<More resources found here: https://www.dataone.org/all-best-practices>
<Delete the text inside the brackets when formatting your file.>

## Summary

This repository stores relevant data sets, and rmarkdown code for analysis of water discharge and sediment loads on the Elwha River. Analysis focuses on the time frame during and after the removal of Glines Canyon Dam and the Elwha Dam, both on the Elwha River, Washington. 

The dataset begins when the removal project begins, September 15, 2011. The Glines Canyon Dam was removed not long after, and the project officially ended on August 26, 2014, but the data was collected until September 30, 2016. Data was recorded by the USGS gage station with identification number- 12046260, which can be found downstream of the old dams sites at the diversion near Port Angeles, Washington.

An understanding of changes on the Elwha River during and following the dam removal process can be understood from analysis on daily water discharge, and parameters surrounding sediment concentration, bedload, size of sediment, and sediment discharge. Looking at changes of these parameters over time in accordance with the time stamps of the project can help explain how long it takes a river to reach a new stability of discharge and sediment discharge following dam removal. 

##Database Information

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
DailyDischarge|Daily water discharge from the river|numeric| m^3^/s
DailySSC | Daily suspended sediment concentration| numeric| mg/L
DailySuspendedSediment| Daily total suspended sediment load|numeric|tonnes
DailySSfines|Daily suspended fine grained sediment load |numeric|tonnes
DailySSsand| Daily suspended sand sediment load|numeric|tonnes
TotalSedimentDischarge|Total daily sediment discharge|numeric|tonnes
Project year| Year of sampling project, extending from 1-5 years|character|year


<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>

## Quality assurance/quality control

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>