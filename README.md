# DAT129_final
## NREL Solar Resource Data API
https://developer.nrel.gov/docs/solar/solar-resource-v1/

#### This program uses the Solar Resource Data API provided by NREL and returns various solar power related parameters for a given latitude and longitude. The goal of the program is to take in a file of lat and long values and iterate through, pulling the values of interest and then writing them to a new file in a format usable for creation of maps and analytical purposes.

DATA RETURNED  
Average Direct Normal Irradiance - measured surface perpendicular to direct solar rays (avg_dni)  
Average Global Horizontal Irradiance - measured surface horizontal to the ground (avg_ghi)  
Average Tilt at Latitude (avg_lat_tilt)


**solar_API_single** allows manual input of lat and long for one off requests  
**solar_API_array2** uses a csv of lat and longs to pull into the API and then saves the data for each into a csv and also takes the yearly data and formats for GIS usage  
**solar_API_array** is the less efficient and less comprehensive version of array2
