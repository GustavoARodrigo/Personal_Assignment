# Personal_Assignment

**Dataset choosed** : [Hourly updated air quality measurements, since 1983](https://data.europa.eu/data/datasets/6a8f6d04-d078-4c27-a84c-f3e1bbc420ed-stadt-zurich?locale=en)

The dataset is about hourly measurements about air quality in Zurich from 1983 to the last current hour divided in annual files. I downloaded the file on December 1, 2022 at about 5 pm, so that will be the date of the last measurements but I will delete December 1, 2022 in order to have only complete months in the dataset. I chose the last five years (2018-2022) due to the fact that the measurements are made hourly, and by 4 different sensors at the same time, and this makes the dataset with to many inputs, and also due to the fact that I am more interested in the evolution in the last five years.
  
The dataset have 7 columns: Datum, Standort, Parameter, Intervall, Einheit, Wert, Status.

Datum-Date Type: Year-Month-DayTHour:Minute+StandardHour, example:2022-12-01T17:00+0100

Standort- Location of where the measurement is done, 4 possible locations: Zch_Heubeeribüel, Zch_Rosengartenstrasse, Zch_Schimmelstrasse, Zch_Stampfenbachstrasse

Parameter- Type of gas, 8 possibles: NO2(Nitrogen dioxide), NO(Nitric oxide), NOx(abbreviation for nitric oxide and nitrogen dioxide), O3(Ozone), PM10(particulate matter), PM2.5(particulate matter 2.5), CO(Carbon Monoxide), SO2(Sulfur dioxide)

Intervall- type of time interval, only 1 possible: h1 (hourly)

Einheit- Unit, 3 possibles: µg/m3(microgram of gaseous pollutant per cubic metre), ppb(parts per billion), mg/m3 (milligram of gaseous pollutant per cubic meter)

Wert- Value of "Parameter" measure with "Einheit"

Status- Measure status, 2 possible: bereinigt(adjusted), provisorisch(provisional)



I consider this dataset interesting because through it is possible to check the air quality and its trend in the last five years, thus being able to see which gases are at dangerous levels and, if that happens, to create measures to reduce the emission of these gases in order to improve the life of the population.

---

**Task want to perform:** 
Check the trend of the most harmful gases for each station, since both are close to the center of Zurich but in different zones.


**Problem to solve:**
Check which gases are at the most dangerous levels and create measures to reduce their emission or create measures to reduce their negative effects.


**Question to be answered:**
Does the variation depend much on the station?Since both are close to the center of Zurich but in different zones.

---

I started by choosing to analyze the variables in the dataset and some statistics.

Then I created new columns for day, month, year, combination of year and month and finally combination of year, month and day to make the analysis and visualization easier.

After creating the new columns, I decided to eliminate December 1, 2022, because I did not consider it relevant to keep only one month with a day that is not even complete. This way the dataset now has only complete months. 


Then I did some visualizations and I could see that:

* Some gases have higher values than desired
* The trends of each gas for the 4 seasons together
* That the status varies between 40.6% corrected and 59.4% provisional
* And that not all gases neither all Stations have the same amount of data which will be explored next






As mentioned, there are 4 stations, all located near Zurich's city center. Description of where each one is located:
* Zch_Stampfenbachstrasse- The measuring station is located in the city center of Zurich. It represents an urban location with moderate traffic. 
* Zch_Schimmelstrasse- The measuring station is located on a main urban traffic axis at a central location in a residential and commercial district of the city of Zurich. It represents an urban location with very heavy traffic.
* Zch_Rosengartenstrasse- The measuring station is located on a main urban traffic axis at a central location in a residential and commercial district of the city of Zurich. It represents an urban location with very heavy traffic
* Zch_Heubeeribüel- The measuring station is located in a school area on a high hill on the outskirts of the city of Zurich, adjacent to an open field towards the Zurichberg forest. The location is representative of residential and recreational areas with little traffic on the edge of large conurbations

The 4 stations have different amounts of inputs, an analysis will be made to analyze what these differences correspond to.

After creating a scatter plot for each station the difference in inputs became evident. This difference exists because not all stations measure the same number of gases.

* Zch_Stampfenbachstrasse- NO2, NO, NOx, O3, PM10, PM2.5, CO, SO2
* Zch_Schimmelstrasse- NO2, NO, NOx, O3, PM10, PM2.5
* Zch_Rosengartenstrasse- NO2, NO, NOx, O3, PM10, PM2..5
* Zch_Heubeeribüel- NO2, NO, NOx, O3


In order to analyze the levels of each gas for each station, a survey was carried out to see which gases are the most dangerous when they are at high levels. In the research it was possible to verify that we have 3 of the gases that are on the list of most dangerous gases. These are NO2, O3 and PM2.5. Both NO2 and O3 are measured at all four stations but PM2.5 is only measured at three of the four stations. 


I chose to do daily analysis in order to see the trend of each gas for each season. The NO2 and O3 thresholds do not change if measured for one hour or for 24 hours, but PM2.5 varies.
Threshols limits for each of the gases to be analyzed (24 hours average)

* NO2:
    * Ideal: NO2 < 50
    * Normal: 50 < NO2 < 100
    * High: 100 < NO2
    
* O3:
    * Ideal: O3 < 65
    * Normal: 65 < O3 < 120
    * High: 120 < O3
    
* PM2.5:
    * Ideal: PM2.5 < 10
    * Normal: 10 < PM2.5 < 20
    * High: 20 < PM2.5


















