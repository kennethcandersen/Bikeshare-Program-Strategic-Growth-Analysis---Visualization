# Bikeshare Program Strategic Growth Analysis & Visualization

<p align="center">
<img src="https://github.com/kennethcandersen/Bikeshare-Program-Strategic-Growth-Analysis-And-Visualization/blob/main/static/Images/ecobici_tour_gif.gif" width="900"/>
</p>

## Team Members
* [Kenneth Andersen](https://github.com/kennethcandersen) 🚴‍♂️ 
* [Uriel Arriaga](https://github.com/Momoyactly) 🚴‍♂️
* [Salvador del Cos](https://github.com/Fispit) 🚴‍♂️
* [Mariana Geffroy López](https://github.com/mgeffroy) 🚴‍♀️
* [Gustavo Maldonado](https://github.com/MBGUS) 🚴‍♂️

## Project summary 

### Project Goal
Apply data analysis & visualization tools to observe the evolution of Mexico City's bike-share program "ECOBICI" and provide recommendations for its future development and growth.

### What is Ecobici? 
ECOBICI is the public bicycle system of Mexico City that has integrated bikes as an essential part of mobility, aimed at inhabitants of the capital and tourists. Since its launch in 2010, Ecobici have provided over 71 million rides in central Mexico City: convenient, sustainable transportation that reduces traffic and pollution and promotes health.

What can you do? Become a rider! Do you live in Mexico City and don't have your ecobici membership yet? [Sign up here](https://www.ecobici.cdmx.gob.mx/es/registro/inicio)

## How to run the app
2 options:
1. **[Fully deployed online version](https://dataviz-ecobici.herokuapp.com/)**: [https://dataviz-ecobici.herokuapp.com/](https://dataviz-ecobici.herokuapp.com/)
2. Run locally:
     1. Clone this repository
     2. In the main repository folder, run "python3 appy.py" in your terminal
     3. Open [http://127.0.0.1:5000/](http://127.0.0.1:5000/) in a browser and the website should launch. 
     4. Browse the website for data visualizations and additional information about the data and team. 

## Original data Sources 📁 
The original data can be found in the following links: 
- [**Ecobici CSV**](https://www.ecobici.cdmx.gob.mx/es/informacion-del-servicio/open-data): ECOBICI trip information by month. Files can be downloaded as CSVs. 
- [**Ecobici API**](https://www.ecobici.cdmx.gob.mx/es/informacion-del-servicio/open-data): The ECOBICI API has information about the 480 stations ( station name, station id, location). 
- [**Open Data Mexico City: Colonias**](https://datos.cdmx.gob.mx/dataset/coloniascdmx): Information about the neighborhoods in Mexico City. We used the "coloniascdmx.csv" file to trace the Colonia boundaries on our map visualizations. 

## ETL process 
#### Extract
- Different datasets concerning our topic were located. Historical data was downloaded in CSV format from the Ecobici website, one file per month.
- Data for each station was downloaded using an the Ecobici API from their website.
#### Transform
- Python was used to unify all of the CSV files (10 years of monthly data) Resulting in 71 million lines. Another python script was used to clean the dataset.
- Given the size of the dataset, we created a subset of one in hundred, resulting in a sample of 710,000 data points.
#### Load
- Data was imported into Postgres.
- Queries regarding stations, general trips, routes and demographics were created.
- Each query was parsed using flask and SQL alchemy and was fed into the webpage using D3.

## Languages used 🖥️
- SQL 
- Javascript
- HTML 
- CSS 
- Python

## Analysis 📈
We decided to analyze demographic data of ECOBICI users as well as most common routes in the ECOBICI network. Different years were analyzed. 

## Preview 🚲
You can move freely around the webpage, so we invite you to explore the data! You can use the navbar, get different information to populate, graphs, tables and maps or whatever you prefer! Have fun!

![image](https://github.com/mgeffroy/P2-Ecobici_insights_and_recommendations/blob/main/static/Images/ecobici_tour_gif.gif)


## Conclusion summary 
- Most Ecobici users are men.
- Most users are in the 20-40 age range. 
- Some stations have traffic and in some areas some are underused. 
- Stations with more traffic are close to metro stations and supermarkets. 




