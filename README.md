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
* And that not all gases have the same amount of data which will be explored next






As mentioned, there are 4 stations, all located near Zurich's city center. Description of where each one is located:
* Zch_Stampfenbachstrasse- The measuring station is located in the city center of Zurich. It represents an urban location with moderate traffic. 
* Zch_Schimmelstrasse- The measuring station is located on a main urban traffic axis at a central location in a residential and commercial district of the city of Zurich. It represents an urban location with very heavy traffic.
* Zch_Rosengartenstrasse- The measuring station is located on a main urban traffic axis at a central location in a residential and commercial district of the city of Zurich. It represents an urban location with very heavy traffic
* Zch_Heubeeribüel- The measuring station is located in a school area on a high hill on the outskirts of the city of Zurich, adjacent to an open field towards the Zurichberg forest. The location is representative of residential and recreational areas with little traffic on the edge of large conurbations

The 4 stations have different amounts of inputs, an analysis will be made to analyze what these differences correspond to


























