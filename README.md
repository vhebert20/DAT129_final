# DAT129_final
## National Renewable Energy Laboratory Solar Resource Data API
https://developer.nrel.gov/docs/solar/solar-resource-v1/

#### This program uses the Solar Resource Data API provided by NREL and returns various solar power related parameters for a given latitude and longitude. The goal of the program is to take in a file of lat and long values and iterate through, pulling the values of interest and then writing them to a new file in a format usable for creation of maps and analytical purposes.  Areas with the highest DNI, GHI, and Lat_TILT can then be determined and targeted for potential solar development.  

#### Specifically for this project, the Direct Normal Irradiance was pulled and mapped to give a general overview of the best location for concentrating solar power (CSP) farms, as DNI is the measurement used to assess potential for this type of solar system.  

#### The sun's energy is concentrated by mirrors/collectors and used to heat oil or salt, which is then used to create steam that runs a traditional turbine for energy creation.  Locations for CSP systems generally need to be larger (+5 acres), and produce 100+ MW of power to be economic.  The DNI also needs to be at least 2000 kWh/m²/year.

https://helioscsp.com/concentrated-solar-power-would-need-to-meet-8-10-of-global-electricity-demand-by-2050/#:~:text=Minimum%20suitable%20DNI%20for%20CSP,of%20sunlight%20are%20much%20lower.  

https://www.nrel.gov/docs/fy10osti/47465.pdf  

https://www.seia.org/initiatives/concentrating-solar-power  

https://solareis.anl.gov/guide/solar/csp/  

__________
**DATA RETURNED**  
Average Direct Normal Irradiance (kWh/m2/day) - measured surface perpendicular to direct solar rays (avg_dni)  
Average Global Horizontal Irradiance (kWh/m2/day) - measured surface horizontal to the ground (avg_ghi)  
Average Tilt at Latitude (kWh/m2/day) - (avg_lat_tilt)  

![DNI_image](https://user-images.githubusercontent.com/71047291/117217248-11004d00-adcf-11eb-9e2c-3cbb660de132.jpg)
https://firstgreenconsulting.wordpress.com/2012/04/26/differentiate-between-the-dni-dhi-and-ghi/  

**ADDITIONAL INFORMATION RESOURCES**  
https://aip.scitation.org/doi/pdf/10.1063/1.4753912  
https://helioscsp.com/steps-for-solar-resource-assessment-in-concentrated-solar-power-projects/  
https://journals.ametsoc.org/view/journals/apme/56/1/jamc-d-16-0175.1.xml  
  
  
**PROGRAM FILES**  
**solar_API_single** allows manual input of lat and long for one off requests  
**solar_API_array2** uses a csv of lat and longs to pull into the API and then saves the data for each into a csv and also takes the yearly data and formats for GIS usage  

_________  
##### TABLE 1: example of reformatted csv with original location information and values returned from the query  

![reformat_example](https://user-images.githubusercontent.com/71047291/117218867-05faec00-add2-11eb-84be-407b66da8f6a.jpg)


##### MAP 1:  mapped average yearly DNI, created from data provided by the API; the southwest US appears to be the only portion of the country that meets the 2000 kWh/m²/year cutoff, based on the data points pulled with the initial data requests    

![yearly_DNI](https://user-images.githubusercontent.com/71047291/117088700-39ca0900-ad21-11eb-9e2d-aced4d6a4b31.jpg)  
