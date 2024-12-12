# <Exploring EJ, Power Plant, and PM2.5 Data Final Project>

## Summary

<This repository contains data and analyses investigating the relationship between coal-burning power plants, PM 2.5 concentrations, and social vulnerability indices (SVI) in North Carolina Counties. This study aims to assess whether areas with higher PM 2.5 levels are correlated with their proximity to coal-burning power plants and if these trends affect communities considered more socially vulnerable as characterized by the CDC. The repository includes cleaned datasets, geospatial analysis outputs, and visualization comparing PM 2.5 levels and SVI across counties.>

## Investigators

<
Lauren Shohan:    
- Affiliation: Duke University Nicholas School of the Environment 
- Contact: lauren.shohan@duke.edu 

Jessalyn Chuang:   
- Affiliation: Duke University Nicholas School of the Environment 
- Contact: jessalyn.chuang@duke.edu 

Alex López:  
- Affiliation: Duke University Nicholas School of the Environment 
- Contact: alex.lopez@duke.edu 
>

## Keywords

<Power Plants, North Carolina, Particulate Matter (PM 2.5), social vulnerability index, environmental justice, air quality>

## Database Information

<
Power Plant Database:  
  - Source: HIFLD GeoPlatform Power Plants Database 
  - Accessed: 11 December 2024 
  - Description: Nationwide data on electric powerplants around the United States and includes relevant information such as primary fuel type, name, location, operational status, plant ID, and plant name.  

Retired Plants Database: 
  - Source: EIA Preliminary Monthly Electric Generator Inventory 
  - Accessed: 11 December 2024 
  - Description: This data source offers monthly updates on the status of electric generators in the United States, maintaining a continuous record of newly added, retired, or modified generating units. 

Social Vulnerability Index Database: 
  - Source: CDC/ATSDR Social Vulnerability (CDC/ATSDR or SVI) data 
  - Accessed: 11 December 2024 
  - Description: Comprehensive information on the social vulnerability of communities in the United States. It includes rankings based on 15 U.S. Census variables grouped into four themes: Socioeconomic Status, Household Composition & Disability, Minority Status & Language, and Housing Type & Transportation.  

PM 2.5 Database:   
  - Source: United States Environmental Protection Agency website’s Outdoor Air Quality Data section
  - Accessed: 11 December 2024 
  - Description: PM 2.5 summary statistics and daily means across counties in North Carolina. 

North Carolina Counties Database:  IF NEEDED 
  - Source: North Carolina Counties Data File
  - Accessed: 11 December 2024 
  - Description: Contains all the locations and names of North Carolina Counties.
>


## Folder structure, file formats, and naming conventions 

<Data Folder: Contains data used in this project. Contains: EPA_PM2.5 folder that contains all the PM2.5 air pollution data, Project_Data folder that contains all the SVI North Carolina data, and retired_generators.csv that contains the years of retirement for NC plants.>

<Wrangling Folder: This folder contains some draft verisons of our wrangling process. There is the PM_wrangling rmd file, powerplant_wrangling rmd file, and then our rough draft proposal_draft rmd file>

<ChuangShohanLopez_FinalProject: There is a RMD file with all the code done for this project and then there is an HTML file named this that can be opened on a web browser. We named this after our three last names.>

## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

1. EPA_PM2.5 Folder, contains data pull from EPA for years 2013-2022

  i. Columns:"Date","Source","Site ID","POC","Daily Mean PM2.5 Concentration","Units","Daily AQI Value","Local Site Name","Daily Obs Count","Percent Complete","AQS Parameter Code","AQS Parameter Description","Method Code","Method Description","CBSA Code","CBSA Name","State FIPS Code","State","County FIPS Code","County","Site Latitude","Site Longitude","FIPS"
  
  ii. Column Meanings: Date: The date of the observation, Source: The source of the air quality data, Site ID: Unique identifier for the monitoring site, POC: Parameter occurrence code identifying the specific parameter monitored, Daily Mean PM2.5 Concentration: Average PM2.5 concentration measured on the given day (µg/m³), Units: Units of measurement for PM2.5 concentration, Daily AQI Value: Air Quality Index value for the day, Local Site Name: Name of the local monitoring site, Daily Obs Count: Number of observations made during the day, Percent Complete: Percentage of complete data for the day, AQS Parameter Code: EPA Air Quality System parameter code for the pollutant, AQS Parameter Description: Description of the parameter monitored, Method Code: Code for the method used to measure PM2.5, Method Description: Description of the measurement method, CBSA Code: Core-Based Statistical Area code for the site location, CBSA Name: Name of the Core-Based Statistical Area, State FIPS Code: Federal Information Processing Standards code for the state, State: Name of the state where the site is located, County FIPS Code: Federal Information Processing Standards code for the county, County: Name of the county where the site is located, Site Latitude: Latitude coordinate of the monitoring site, Site Longitude: Longitude coordinate of the monitoring site, FIPS: Combined state and county FIPS code for the site
  
  iii. Class of data: Date: chr, Source: chr, Site ID: num, POC: num, Daily Mean PM2.5 Concentration: num, Units: chr, Daily AQI Value: num, Local Site Name: chr, Daily Obs Count: num, Percent Complete: num, AQS Parameter Code: num, AQS Parameter Description: chr, Method Code: num, Method Description: chr, CBSA Code: num, CBSA Name: chr, State FIPS Code: num, State: chr, County FIPS Code: chr, County: chr, Site Latitude: num, Site Longitude: num, FIPS: chr
  
  iv. Units: Daily Mean PM2.5 Concentration: µg/m³ (micrograms per cubic meter), Units: µg/m³ LC (micrograms per cubic meter, Local Conditions), Daily AQI Value: Index value (Air Quality Index scale), Site Latitude: Decimal degrees, Site Longitude: Decimal degrees
  
2. Project_Data folder contains SVI data pulls from the CDC for North Carolina for each of the following years: 2010, 2014, 2016, 2018, 2020, 2022

NorthCarolina_county_2014.csv file:

  i. Columns:
"AFFGEOID", "ST", "STATE", "ST_ABBR", "COUNTY", "FIPS", "LOCATION", "AREA_SQMI", "E_TOTPOP", "M_TOTPOP", "E_HU", "M_HU", "E_HH", "M_HH", "E_POV", "M_POV", "E_UNEMP", "M_UNEMP", "E_PCI", "M_PCI", "E_NOHSDP", "M_NOHSDP", "E_AGE65", "M_AGE65", "E_AGE17", "M_AGE17", "E_DISABL", "M_DISABL", "E_SNGPNT", "M_SNGPNT", "E_MINRTY", "M_MINRTY", "E_LIMENG", "M_LIMENG", "E_MUNIT", "M_MUNIT", "E_MOBILE", "M_MOBILE", "E_CROWD", "M_CROWD", "E_NOVEH", "M_NOVEH", "E_GROUPQ", "M_GROUPQ", "EP_POV", "MP_POV", "EP_UNEMP", "MP_UNEMP", "EP_PCI", "MP_PCI", "EP_NOHSDP", "MP_NOHSDP", "EP_AGE65", "MP_AGE65", "EP_AGE17", "MP_AGE17", "EP_DISABL", "MP_DISABL", "EP_SNGPNT", "MP_SNGPNT", "EP_MINRTY", "MP_MINRTY", "EP_LIMENG", "MP_LIMENG", "EP_MUNIT", "MP_MUNIT", "EP_MOBILE", "MP_MOBILE", "EP_CROWD", "MP_CROWD", "EP_NOVEH", "MP_NOVEH", "EP_GROUPQ", "MP_GROUPQ", "EPL_POV", "EPL_UNEMP", "EPL_PCI", "EPL_NOHSDP", "SPL_THEME1", "RPL_THEME1", "EPL_AGE65", "EPL_AGE17", "EPL_DISABL", "EPL_SNGPNT", "SPL_THEME2", "RPL_THEME2", "EPL_MINRTY", "EPL_LIMENG", "SPL_THEME3", "RPL_THEME3", "EPL_MUNIT", "EPL_MOBILE", "EPL_CROWD", "EPL_NOVEH", "EPL_GROUPQ", "SPL_THEME4", "RPL_THEME4", "SPL_THEMES", "RPL_THEMES", "F_POV", "F_UNEMP", "F_PCI", "F_NOHSDP", "F_THEME1", "F_AGE65", "F_AGE17", "F_DISABL", "F_SNGPNT", "F_THEME2", "F_MINRTY", "F_LIMENG", "F_THEME3", "F_MUNIT", "F_MOBILE", "F_CROWD", "F_NOVEH", "F_GROUPQ", "F_THEME4", "F_TOTAL", "E_UNINSUR", "M_UNINSUR", "EP_UNINSUR", "MP_UNINSUR", "E_DAYPOP", "Shape", "Shape.STArea..", "Shape.STLength.."

For simplicity, this study focused on the following columns: RPL_THEME1, RPL_THEME2, RPL_THEME3, RPL_THEME4, and RPL_THEMES. Descriptions for these specific columns are provided below, while the others are excluded.

  ii. Column Meanings: RPL_THEME1: Socioeconomic Theme, RPL_THEME2: Household Composition and Disability Theme, RPL_THEME3: Minority Status and Language Theme, RPL_THEME4: Housing and Transportation, RPL_THEMES: overall summary ranking variable that is an aggregate of the four themes
  
  iii. Class of data: RPL_THEME1: num, RPL_THEME2: num, RPL_THEME3: num, RPL_THEME4: num, RPL_THEMES: num
  
  iv. Units: These unitless indices represent percentiles, where higher values indicate greater vulnerability within each theme. The aggregate index reflects overall social vulnerability.
  
SVI geodatabase (gdb) files:

  i. Columns:"ST", "STATE", "ST_ABBR", "COUNTY", "FIPS", "LOCATION", "AREA_SQMI", "E_TOTPOP", "M_TOTPOP", "E_HU", "M_HU", "E_HH", "M_HH", "E_POV", "M_POV", "E_UNEMP", "M_UNEMP", "E_PCI", "M_PCI", "E_NOHSDP", "M_NOHSDP", "E_AGE65", "M_AGE65", "E_AGE17", "M_AGE17", "E_DISABL", "M_DISABL", "E_SNGPNT", "M_SNGPNT", "E_MINRTY", "M_MINRTY", "E_LIMENG", "M_LIMENG", "E_MUNIT", "M_MUNIT", "E_MOBILE", "M_MOBILE", "E_CROWD", "M_CROWD", "E_NOVEH", "M_NOVEH", "E_GROUPQ", "M_GROUPQ", "EP_POV", "MP_POV", "EP_UNEMP", "MP_UNEMP", "EP_PCI", "MP_PCI", "EP_NOHSDP", "MP_NOHSDP", "EP_AGE65", "MP_AGE65", "EP_AGE17", "MP_AGE17", "EP_DISABL", "MP_DISABL", "EP_SNGPNT", "MP_SNGPNT", "EP_MINRTY", "MP_MINRTY", "EP_LIMENG", "MP_LIMENG", "EP_MUNIT", "MP_MUNIT", "EP_MOBILE", "MP_MOBILE", "EP_CROWD", "MP_CROWD", "EP_NOVEH", "MP_NOVEH", "EP_GROUPQ", "MP_GROUPQ", "EPL_POV", "EPL_UNEMP", "EPL_PCI", "EPL_NOHSDP", "SPL_THEME1", "RPL_THEME1", "EPL_AGE65", "EPL_AGE17", "EPL_DISABL", "EPL_SNGPNT", "SPL_THEME2", "RPL_THEME2", "EPL_MINRTY", "EPL_LIMENG", "SPL_THEME3", "RPL_THEME3", "EPL_MUNIT", "EPL_MOBILE", "EPL_CROWD", "EPL_NOVEH", "EPL_GROUPQ", "SPL_THEME4", "RPL_THEME4", "SPL_THEMES", "RPL_THEMES", "F_POV", "F_UNEMP", "F_PCI", "F_NOHSDP", "F_THEME1", "F_AGE65", "F_AGE17", "F_DISABL", "F_SNGPNT", "F_THEME2", "F_MINRTY", "F_LIMENG", "F_THEME3", "F_MUNIT", "F_MOBILE", "F_CROWD", "F_NOVEH", "F_GROUPQ", "F_THEME4", "F_TOTAL", "E_UNINSUR", "M_UNINSUR", "EP_UNINSUR", "MP_UNINSUR", "E_DAYPOP", "Shape_Length", "Shape_Area", "GDB_GEOMATTR_DATA", "Shape"
  
  ii. Column Meanings: RPL_THEME1: Socioeconomic Theme, RPL_THEME2: Household Composition and Disability Theme, RPL_THEME3: Minority Status and Language Theme, RPL_THEME4: Housing and Transportation, RPL_THEMES: overall summary ranking variable that is an aggregate of the four themes, Shape: contains spatial information for mapping
  
  iii. Class of data: RPL_THEME1: num, RPL_THEME2: num, RPL_THEME3: num, RPL_THEME4: num, RPL_THEMES: num, Shape: sfc_MULTIPOLYGON
  
  iv. Units: The unitless indices represent percentiles, where higher values indicate greater vulnerability within each theme. The aggregate index reflects overall social vulnerability. Geodetic CRS of "Shape"" is NAD83, which uses latitude and longitude in degrees as its units.
  
3. API endpoint from ArcGIS FeatureServer: https://services1.arcgis.com/Hp6G80Pky0om7QvQ/arcgis/rest/services/Plants_gdb/FeatureServer/0/query?outFields=*&where=1%3D1&f=geojson

  i. Columns: "OBJECTID", "PLANT_CODE", "NAME", "ADDRESS", "CITY", "STATE", "ZIP", "TELEPHONE", "TYPE", "STATUS", "COUNTY", "COUNTYFIPS", "COUNTRY", "LATITUDE", "LONGITUDE", "NAICS_CODE", "NAICS_DESC", "SOURCE", "SOURCEDATE", "VAL_METHOD", "VAL_DATE", "WEBSITE", "OPERATOR", "OPERAT_ID", "OPER_CAP", "SUMMER_CAP", "WINTER_CAP", "PLAN_CAP", "RETIRE_CAP", "GEN_UNITS", "PLAN_UNIT", "RETIR_UNIT", "PRIM_FUEL", "SEC_FUEL", "COAL_USED", "NGAS_USED", "OIL_USED", "NET_GEN", "CAP_FACTOR", "SUB_1", "SUB_2", "LINES", "SOURCE_LAT", "SOURC_LONG", "geometry"
  
  ii. Column Meanings: OBJECTID: Unique identifier for the plant record, PLANT_CODE: Unique code for the power plant, NAME: Name of the power plant, ADDRESS: Street address of the plant, CITY: City where the plant is located, STATE: State where the plant is located, ZIP: ZIP code of the plant's location, TELEPHONE: Contact telephone number for the plant, TYPE: Type of plant (e.g., power generation, distribution), STATUS: Operational status of the plant (e.g., active, retired), COUNTY: County where the plant is located, COUNTYFIPS: FIPS code for the county, COUNTRY: Country where the plant is located, LATITUDE: Latitude coordinate of the plant, LONGITUDE: Longitude coordinate of the plant, NAICS_CODE: Industry classification code for the plant, NAICS_DESC: Description of the plant's NAICS classification, SOURCE: Source of the plant's data, SOURCEDATE: Date the data was sourced, VAL_METHOD: Validation method for the data, VAL_DATE: Date of data validation, WEBSITE: Website associated with the plant or operator, OPERATOR: Name of the operator managing the plant, OPERAT_ID: Unique identifier for the operator, OPER_CAP: Operational capacity of the plant, SUMMER_CAP: Plant's capacity during summer, WINTER_CAP: Plant's capacity during winter, PLAN_CAP: Planned capacity of the plant, RETIRE_CAP: Capacity at the time of retirement, GEN_UNITS: Number of generation units at the plant, PLAN_UNIT: Number of planned units at the plant, RETIR_UNIT: Number of retired units at the plant, PRIM_FUEL: Primary fuel type used by the plant, SEC_FUEL: Secondary fuel type used by the plant, COAL_USED: Amount of coal used by the plant, NGAS_USED: Amount of natural gas used by the plant, OIL_USED: Amount of oil used by the plant, NET_GEN: Net electricity generation of the plant, CAP_FACTOR: Capacity factor of the plant, SUB_1: Additional attribute (specific meaning depends on the dataset), SUB_2: Additional attribute (specific meaning depends on the dataset), LINES: Number of transmission lines connected to the plant, SOURCE_LAT: Source latitude coordinate for the data, SOURC_LONG: Source longitude coordinate for the data, geometry: Spatial geometry information for mapping.
  
  iii. Class of data: OBJECTID: int, PLANT_CODE: chr, NAME: chr, ADDRESS: chr, CITY: chr, STATE: chr, ZIP: chr, TELEPHONE: chr, TYPE: chr, STATUS: chr, COUNTY: chr, COUNTYFIPS: chr, COUNTRY: chr, LATITUDE: num, LONGITUDE: num, NAICS_CODE: chr, NAICS_DESC: chr, SOURCE: chr, SOURCEDATE: num, VAL_METHOD: chr, VAL_DATE: num, WEBSITE: chr, OPERATOR: chr, OPERAT_ID: chr, OPER_CAP: num, SUMMER_CAP: num, WINTER_CAP: num, PLAN_CAP: num, RETIRE_CAP: num, GEN_UNITS: int, PLAN_UNIT: int, RETIR_UNIT: int, PRIM_FUEL: chr, SEC_FUEL: chr, COAL_USED: int, NGAS_USED: int, OIL_USED: int, NET_GEN: num, CAP_FACTOR: num, SUB_1: chr, SUB_2: chr, LINES: int, SOURCE_LAT: num, SOURC_LONG: num, geometry: sfc_POINT
  
  iv. Units: LATITUDE: degrees, LONGITUDE: degrees, SOURCEDATE: timestamp (epoch time), VAL_DATE: timestamp (epoch time), OPER_CAP: megawatts (MW), SUMMER_CAP: megawatts (MW), WINTER_CAP: megawatts (MW), PLAN_CAP: megawatts (MW), RETIRE_CAP: megawatts (MW), COAL_USED: short tons, NGAS_USED: thousand cubic feet (Mcf), OIL_USED: barrels (bbl), NET_GEN: megawatt-hours (MWh), CAP_FACTOR: unitless (percentage as a decimal)

4. retired_generators.csv

  i. Columns: "Plant.Name", "Plant.ID", "Retirement.Year"
  
  ii. Column Meanings: Plant.Name: Name of Plant, Plant.ID: Plant's ID as designated by the DOE, Retirement.Year: Year that the unit retired
  
  iii. Class of data: Plant.Name: chr, Plant.ID: int, Retirement.Year: int
  
  iv. Units: Unitless data

5. cb_2018_us_county_20m.shp

  i. Columns: "STATEFP", "COUNTYFP", COUNTYNS", "AFFGEOID", "GEOID", "COUNTY", "LSAD", "ALAND", "AWATER", "geometry"
  
  ii. Column Meanings: STATEFP: State FIPS code, COUNTYFP: County FIPS code, COUNTYNS: County ANSI feature identifier, AFFGEOID: Full geographic identifier, GEOID: Combined state and county FIPS code, COUNTY: Name of the county, LSAD: Legal/statistical area description, ALAND: Land area in square meters, AWATER: Water area in square meters, geometry: Spatial geometry information for mapping
  
  iii. Class of data: STATEFP: chr, COUNTYFP: chr, COUNTYNS: chr, AFFGEOID: chr, GEOID: chr, COUNTY: chr, LSAD: chr, ALAND: num, AWATER: num, geometry: sfc_MULTIPOLYGON
  
  iv. Units: Geodetic CRS of "geometry" is NAD83, which uses latitude and longitude in degrees as its units.

## Scripts and code

Wrangling Folder: 
1. PM_Wrangling.Rmd: wrangling of PM2.5 data
2. PowerPlant_Wrangling.Rmd: wrangling of power plant data
3. Proposal_Draft.Rmd: Contains wrangling of SVI data along with first draft of proposal (visual and statistical analysis)

Final Project Output: ChuangShohanLopez_FinalProject.Rmd
