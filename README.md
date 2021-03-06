# EDA_Project
# The Relationship Between Eight Biomarkers and Exposure to Ozone and PM2.5


## Summary

A previous study was conducted to examine the association between ozone exposure and cardiopulmonary pathophysiologic mechanisms in 2017 Changsha, China. We have analyzed three more biomarkers in Changsha samples to compare the health effects of PM2.5 and ozone or both. There are R-markdown files of the code, and two folders, one is for the data, the other is for the output files in this repository. In the R-markdown files, I have wrangled and tidied the raw data, built full models for each biomarker and optimized them, then explored the correlation between pollutant exposure and biomarkers.


## Investigators

Xiangtian Wang, Ph.D. students of NSOE, xiangtian.wang@duke.edu, lab and data analyst
Yang Wang, MS students of NSOE, yang.wang@duke.edu, lab and data analyst
Dr Zhang, Professor of NSOE, junfeng.zhang@duke.edu, PI


## Keywords

Ozone; PM2.5; Exposure; Biomarker; Cardiovascular; linear regression model

## Database Information

The previous data are from two files "changsha_blood.csv" and "changsha_urine.csv" that contain the demographics data and average exposure data and the concentrations of 5 biomarkers. These two files are combined with our new experimental data of three biomarkers into the data file, "changsha_2020.csv".

## Folder structure, file formats, and naming conventions 

There are R-markdown files of the code, and two folders, one is for the data, the other is for the output pdf or jpeg files in this repository.

In the root folder, there are R-project and readme, and the R-markdown files.

In the "data" folder, there are CSV files that contain the raw and processed data.
In the "output" folder, there are output pdf and graphs generated by R.
 

I used the project name, function, and date as my naming conventions.

## Metadata
We have three csv data source, the changsha_urine and changsha_blood include the almost same variables except different biomarkers. In urine file has "ohdg" and "mda", in blood file has "psel","CRP",and "VWR". In our lab data file, we have three new biomarkers data.

Each column's description as below: 
Variable	Description
Sample_ID	the identity number of the samples
Subject ID	the identity number of the subjects
visit	visit
group	group
COLD	cold ( represent respiratory infection)
MNST	whether or not having menstration during visit
last.ate	the hours to the last meal
wkday.start	the day that the subject start their work
go.home	the day that the subject go home
Smoker	a smoker or not
ExSmoker	used to be a smoker or not
dt_smoke	second-hand smoke exposure in hours
USG	urine specific gravity
o3exp.12h	the exposure of ozone in 12h
pmexp.12h	the exposure of PM2.5 in 12h
no2exp.12h	the exposure of NO2 in 12h
so2exp.12h	the exposure of SO2 in 12h
Temp.12h	temperature in 12h
RHx.12h	humidity in 12h
o3exp.24h	the exposure of ozone in 24h
pmexp.24h	the exposure of PM2.5 in 24h
no2exp.24h	the exposure of NO2 in 24h
so2exp.24h	the exposure of SO2 in 24h
Temp.24h	temperature in 24h
RHx.24h	humidity in 24h
o3exp.1w	the exposure of ozone in one week
pmexp.1w	the exposure of PM2.5 in one week
no2exp.1w	the exposure of NO2 in one week
so2exp.1w	the exposure of SO2 in one week
Temp.1w	temperature in one week
RHx.1w	humidity in one week
o3exp.2w	the exposure of ozone in two weeks
pmexp.2w	the exposure of PM2.5 in two weeks
no2exp.2w	the exposure of NO2 in two weeks
so2exp.2w	the exposure of SO2 in two weeks
Temp.2w	temperature in two weeks
RHx.2w	humidity in two weeks
psel	P-selectin (sCD62P)
CRP	C-reactive protein 
VWF	von Willebrand factor 
OHdG	8-hydroxy-2’-deoxyguanosine 
MDA	malondialdehyde
isoprostane	8-iso-prostaglandin F2 alpha 
HEHE	hepatic epithelioid haemangioendothelioma
TxB2	11-dehydro-thromboxane B2 

## Scripts and code

Changsha_data.Rmd Wrangling and tidying the raw data
Changsha2.Rmd     Exploring the regression models
Wang_Project.Rmd  Output the report

## Quality assurance/quality control

All the lab data follow the QA/QC in the lab.
Then mark all the below detection limit and the above detection limit as NA.  When we combined the three CSV files, "changsha_urine", "changsha_blood" and "changsha_2020", all the NA have been omitted. We have 306 available rows of data. Then we checked the normal distribution of the concentration of biomarkers. Each of eight biomarkers requires to transform into the logarithm. After the transformation, there are no obvious outliers. In this project, the significant statistics are default as p-value< 0.05.