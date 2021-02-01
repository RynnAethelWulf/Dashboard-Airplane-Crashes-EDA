<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://i.imgur.com/6wj0hh6.jpg" alt="Project logo"></a>
</p>

<h3 align="center">Exploratory Data Analysis of Airline crashes using ETL method,data storage using  PostgresSQL and displaying data in a clean interactive dashboard. </h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/kylelobo/The-Documentation-Compendium.svg)](https://github.com/bimalkprabha/Dashboard-Airplane-Crashes-EDA/issues)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> The project kicked-off with an intention to analyze the available data of airline crashes from 1908 till 2019.

  
</p>

## 📝 Table of Contents

- [Team](#Team)
- [Objective](#about)
- [Getting Started](#getting_started)
- [Bonus](#bonus)
- [Acknowledgments](#acknowledgement)

## 🧐 Team Members <a name = "Team"></a>
1. Divya
2. Warren
3. Kelly
4. Bimal

## :ledger: Objective <a name = "about"></a>

Exploratory data analysis for plane crashes between 1908 and 2019 investigating on underlying reasons, location of events and finding trends if any.

### Hypothesis
Is there any link between the different time periods and the fatality rate? </br>

What has been the overall trend for air travel fatalities by country? </br>

What are the most dangerous aircraft operators? </br>

Which Aircraft types were most represented in accidents? </br>

Which countries had the most accidents? </br>

### Extraction
Data was extracted from a Kaggle csv and contained data from 1908 to 2020.

#### Transforming
The following cleaning was done using Jupyter notebooks:
- Dropping columns for readability.
- Formatting of dates using timestamp
- Calculation and addition of a fatality rate column
- Binning by 20-year periods with a corresponding column for sorting.
- String splitting to extract origin airports for origin column.
- Processing using GeoPY module for geolocation data of countries.
- Dropping of null values as well as fixing location data, as some entries were null due to crashes in international waters.

#### Loading
- The data was loaded into Postgres using SQL alchemy
- API Endpoints were created using flask.

#### Visualization techniques <br>
1. Python Flask-powered API -Endpoints created with server-side rendering.
2. HTML , Plot.ly ,Geopy ,Apex.js and D3 used in combination for creating visuals including graphs and charts.

## 🏁 Getting Started <a name = "getting_started"></a>

#### ERD - Diagram <br>

![Comparison](EmployeeSQL/QuickDBD.PNG) <br>

ERD Diagram establishing the realtionship between the tables. <br>

## Bonus Part -Importing the SQL database into Pandas. <a name = "bonus"></a>

A bar chart of average salary by title. <br>

![Comparison Hist](EmployeeSQL/avgsallarytitle.png) <br>

Histogram to visualize the most common salary ranges for employees.<br>

![Salary](EmployeeSQL/salarydist.png) <br>



### Conclusion 
1. An Increase in the number of fatalities recorded after 1945 observed. This could be the increased no. of flights and high mobility after WW2.

2. The countries with high frequency of flights and busier routes like US; rough terrain and weather conditions(Russia) and poor flight safety standards or regulatory regime(Colombia) had largest fatalities reported.

3. Operators - Aeroflot and Air France came out as the notorious ones for causing maximum fatalities in the crashes. Further investigations required to ascertain the reasons for the above.

4. Aircraft types caused most fatalities- Douglas Dc-3; followed by De Havilland Canada

5. The following years are noted for the largest no. of fatalities reported:-</br>
1972 – 5166 fatalities; 62 incidents
- Avg fatality rate per incident = 83.32%
1985 – 4860 fatalities
1996 – 4376 fatalities
2000 – 2786 fatalities; 57 incidents
- Avg fatality rate per incident = 48.87%
2014 - 2248 fatalities


## 🎉 Acknowledgements <a name = "acknowledgement"></a>
- UWA Data Science
- Kaggle
- Team Members
