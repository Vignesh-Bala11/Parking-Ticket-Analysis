# Parking-Ticket-Analysis

Description:
Visualizing parking infractions in Toronto for the year 2016 using python and Tableau


Vizulation Link : https://public.tableau.com/views/2016_Parking_Analysis/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link


Quality Assurance Document:

The goal of the project is to analyze parking infractions in the city of Toronto.  The first step in analysis was to determine the quality of the Parking tickets excel file and the Toronto neighborhood shapes files as those were the primary sources of data to carry out the project. Initial analysis of the neighborhoods shape file showed that there were no missing values and that data in each column was representative of the assigned datatype (integer column had integer datatypes). Secondly no null values were detected in the dataset meaning no heavy pre-processing was required. The parking tickets data set was considerably worse as there were many null values as well as wrong datatypes in each column.  First step to clean the data was to convert the data column into and appropriate format and drop null values from the location column and neighborhood identification column as my end project dataset would be a merged file between the parking tickets and the neighborhood shape files. Once the data column was cleaned, efforts went towards dropping irrelevant columns as well as cleaning up the time values as they were float datatypes rather than a date-time datatype. Time was a float datatype but interpreted as 24-hour clock notation, so logic was preformed to convert float to date-time datatype. One limitation found with data-time was each timestamp as assigned a data starting from January 1, 1900, so decided to convert time to string data type to slice out the date stamp. Once data was cleaned quality test were preformed to verify integrity and quality of the data. One step prior to importing data onto tableau to generate visualizations was the merger of the new cleaned data set and the neighbors shape file and exporting a sub dataset which contained fine amounts for each infraction. The final dataset after cleaning the initial consisted of 516,460 entries compared to the original 700,000 which not only saves memory but a more indicative representation of the parking infractions in Toronto demonstrated in the visualizations.
