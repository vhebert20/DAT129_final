# DAT129_final
## NREL Solar Resource Data API
https://developer.nrel.gov/docs/solar/solar-resource-v1/

#### This program uses the Solar Resource Data API provided by NREL and returns various solar power related parameters for a given latitude and longitude. The goal of the program is to take in a file of lat and long values and iterate through, pulling the values of interest and then writing them to a new file in a format usable for creation of maps and analytical purposes.  Areas with the highest DNI, GHI, and Lat_TILT can then be determined and targeted for potential solar development.

**DATA RETURNED**  
Average Direct Normal Irradiance - measured surface perpendicular to direct solar rays (avg_dni)  
Average Global Horizontal Irradiance - measured surface horizontal to the ground (avg_ghi)  
Average Tilt at Latitude (avg_lat_tilt)

  
**PROGRAM FILES**  
**solar_API_single** allows manual input of lat and long for one off requests  
**solar_API_array2** uses a csv of lat and longs to pull into the API and then saves the data for each into a csv and also takes the yearly data and formats for GIS usage  

  
##### TABLE 1: example of reformatted csv with original location information and values returned from the query  

![reformat_example](https://user-images.githubusercontent.com/71047291/117088832-9c230980-ad21-11eb-98af-ec44e9b80c01.jpg)  


##### MAP 1:  example of mapped average yearly DNI, created from data provided by the API; as would be expected - the southwest US has highest values  

![yearly_DNI](https://user-images.githubusercontent.com/71047291/117088700-39ca0900-ad21-11eb-9e2d-aced4d6a4b31.jpg)  
