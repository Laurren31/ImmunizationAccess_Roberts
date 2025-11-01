# ImmunizationAccess_Roberts
README: Accessibility of Immunization Across Calgary 

Project overview:
The access to vaccination sites indicator examines the spatial dimensions of public health equity, exploring whether income influences the accessibility of immunization services. This analysis compares the spatial distribution of vaccination sites with median household income across Calgary’s Community Service Areas (CSAs) to identify potential disparities in the availability of services. Namely, this indicator seeks to answer the question: To what extent does household income affect access to immunization within Calgary? 

Folder structure: 
Within the main folder resides 3 subfolders: Data, Documents, and Output Figures. 
- All data will be stored in the “Data” folder. Within this folder there are two subfolders: “Raw Data”: this folder contains all the unedited raw data directly from the source; and Processed Data: this folder includes edited intermediate and final data, as well as associated metadata and schemas. 
- The “Documents” folder holds documents such as the README, a written report including results and findings, and a citations document.
- The “Output_Figures” folder contains two subfolders: the “Graphs” folder holds output scatterplot and boxplot graphs; the “Maps” folder contains output map layouts. 

CRS and Data Format:
- Processed data is formatted as CSV files while the raw data is mostly Shapefiles. 
- All data was projected using NAD 1983 CSRS UTM Zone 11N.
- The CEI is completed over a Community Service Areas: custom geography made from combining two adjacent census tracts to reach ~10,000 people. 

Data sources: 
- Vaccination Locations: sourced from Calgary Open Data Portal, data provided by Blue Cross, Accessed October 16, 2025
- Median Income: source from Calgary Open Data Portal, data provided by Calgary Equity Index Overlay Statistics, Accessed October 16, 2025
- 2021 Federal Population and Dwelling Count by Community: sources for Statistics Canada, data provided by the 2021 Federal Census, Accessed October 17, 2025

Methods summary:
This analysis was completed using ArcGIS Pro and Excel using a modified proximity-based approach. Buffer zones of 1 km were created around each immunization site and population count was calculated for each catchment. Population calculations were completed under the assumption of uniform distribution of individuals and used Euclidean distances. Using the population counts of each catchment, accessibility scores were calculated. This analysis defines accessibly scores as the number of vaccinations sites available per 1,000 individuals. Following this, an ANOVA: Single Factors analysis was completed to determine if the null hypothesis of no statistically significant relationship between median income and spatial access could be rejected or accepted.  
- Detailed methodology can be found in the WrittenReport_Accessibility_of_Immunization

Alphabetical Field Dictionary: 
- ANTIVIRAL: if antiviral is offered at vaccination site. 
- AREA_Type: type of area values is measured in; in this case it is CSA. 
- AREA_ID: ID for area location
- ATTRIBUTE: the CEI is measures many indicators, in this case the indicator selected is median income
- BUFFER_DISTANCE: size of buffer around each vaccination site
- BUFF_SHAPE_LENGTH: shape length of buffer pieces 
- BUFF_SHAPE_AREA: shape area of buffer pieces
- CATEGORY: Class of indicator 
- CEI_RANKING: quartile ranking determined by CEI for each CSA by median income. 
- CITY: city vaccination site is located in 
- COMMUNITY_ABRV: abbreviated community name 
- COMMUNITY_FULL: full community name 
- COVID_19: If Covid-19 vaccinations are offered at vaccination location
- DA_AREA_m2: area of dissemination area in meters squared
- DATA_CURRENCY: information on the year or date data was procured. 
- Fields:  COVID-19, RSV, TDAP and PNEUMOCCOCAL: if this type of vaccination is available in each vaccination site 
- JOIN_COUNT: How many features from the join layer were matches to the target layer
- JOIN_FID: ID of the joined feature
- MEAN_VS_PER_1000: mean value of vaccination sites per 1000 people. 
- OJECTID: the CSA number (1 through 113)
- PHONE: phone number of vaccination site
- QUARTILE_RANKING: quartile ranking derived from Natural Breaks (Jenks) 
- SUM_POP_CATCHMENT_PIECE: population covered by each buffer
- TARGET_FID: ID of the target feature from join
- VALUE: median income value 
- VALUE_LABEL: median income value distinguished by data type (currency)
- NEAR_FID: FID of nearest vaccination site
- NEAR_DIST: nearest distance in meters
- VS_ID: Lettered ID for vaccination sites 
- VS_NAME: name of vaccination site 
- VS_ADDRESS1: vaccination site address
- VS_ADDRESS2: secondary vaccination site address if applicable
- VS_PER_1000: raw amount of vaccination sites per 1000 people
- VS_PER_1000_FILLED: null values removed and replaced with 0

Licence and Citation:
- In depth citation information are in the “Citations” document within the “Documents” folder
- This work can be sited as follows: Lauren Roberts 2025, Accessibility of Immunization Across Calgary, https://github.com/Laurren31/ImmunizationAccess_Roberts 
- Accessibility of Immunization Across Calgary © 2025 by Lauren Roberts is licensed under CC BY 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by/4.0/

Contact: 
Lauren Roberts at Lauren.c.Roberts31@gmail.com 
