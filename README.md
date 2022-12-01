# Personal_Assignment

**Dataset choosed** : [Hourly updated air quality measurements, since 1983](https://data.europa.eu/data/datasets/6a8f6d04-d078-4c27-a84c-f3e1bbc420ed-stadt-zurich?locale=en)

The dataset is about hourly measurements about air quality in Zurich from 1983 to the last current hour divided in annual files. I downloaded the file on December 1, 2022 at about 5 pm, so that will be the date of the last measurements. I chose the last five years (2018-2022) due to the fact that the measurements are made hourly, and by 4 different sensors at the same time, and this makes the dataset with to many inputs, and also due to the fact that I am more interested in the evolution in the last five years.
  
The dataset have 7 columns: Datum, Standort, Parameter, Intervall, Einheit, Wert, Status.

Datum-Date Type: Year-Month-DayTHour:Minute+StandardHour, example:2022-12-01T17:00+0100

Standort- Location of where the measurement is done, 4 possible locations: Zch_Heubeeribüel, Zch_Rosengartenstrasse, Zch_Schimmelstrasse, Zch_Stampfenbachstrasse

Parameter- Type of gas, 8 possibles: NO2(Nitrogen dioxide), NO(Nitric oxide), NOx(abbreviation for nitric oxide and nitrogen dioxide), O3(Ozone), PM10(particulate matter), PM2.5(particulate matter 2.5), CO(Carbon Monoxide), SO2(Sulfur dioxide)

Intervall- type of time interval, only 1 possible: h1 (hourly)

Einheit- Unit, 3 possibles: µg/m3(microgram of gaseous pollutant per cubic metre), ppb(parts per billion), mg/m3 (milligram of gaseous pollutant per cubic meter)

Wert- Value of "Parameter" measure with "Einheit"

Status- Measure status, 2 possible: bereinigt(adjusted), provisorisch(provisional)















