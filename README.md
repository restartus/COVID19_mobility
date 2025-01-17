# COVID-19 Mobility Data Aggregator. Scraper of Google, Apple and Waze COVID-19 Mobility Reports
This is a repository with a data scraper of Mobility Reports and reports in different formats.

## Table of contents
1. [ About data ](#About_data)
    * [ 1. About Google COVID-19 Community Mobility Reports](#about_google_data)
    * [ 2. About Apple COVID-19 Mobility Trends Reports](#about_apple_data)
    * [ 3. About Waze COVID-19 local driving trends](#about_waze_data)
2. [ Data explorer ](#data_explorer)
    * [ 1. Google Reports](#google_reports)
    * [ 2. Apple Reports](#apple_reports)
    * [ 3. Waze Reports](#waze_reports)
    * [ 4. Summary Reports](#summary_reports)
3. [ How to run script ](#how_to_run_script)
4. [ Contributing ](#contributing)
5. [ Showcases ](#showcases)
    * [ 1. Dashboards and visualizations based on these data](#visualisations)
    * [ 2. Articles and research publications](#articles)

## About data
<a name="About_data"></a>

### About [Google COVID-19 Community Mobility Reports](https://www.google.com/covid19/mobility/)
<a name="about_google_data"></a>
In early April 2020, Google started publishing an early release of COVID-19 Community Mobility Reports to provide insights into what has changed in response to work from home, shelter in place, and other policies aimed at flattening the curve of this pandemic. These reports have been developed to be helpful while adhering to our stringent privacy protocols and policies. 

These Community Mobility Reports aim to provide insights into what has changed in response to policies aimed at combating COVID-19. The reports chart movement trends over time by geography, across different categories of places such as retail and recreation, groceries and pharmacies, parks, transit stations, workplaces, and residential.

**Update interval:** twice a week

By downloading or using this data and reports, you agree to Google [Terms of Service](https://policies.google.com/terms).

### About [Apple COVID-19 Mobility Trends Reports](https://www.apple.com/covid19/mobility)
<a name="about_apple_data"></a>
The CSV file shows a relative volume of directions requests per country/region or city compared to a baseline volume on January 13th, 2020.

Day defined as midnight-to-midnight, Pacific time. Cities represent usage in greater metropolitan areas and are stably defined during this period. In many countries/regions and cities, relative volume has increased since January 13th, consistent with normal, seasonal usage of Apple Maps. Day of week effects are important to normalize as you use this data.

Data that is sent from users' devices to the Maps service is associated with random, rotating identifiers so Apple doesn't have a profile of your movements and searches. Apple Maps has no demographic information about Apple users, so it's impossible to make any statements about the representativeness of usage against the overall population.

**Update interval:** daily

By downloading or using this data, you agree to Apple terms.


### About [Waze COVID-19 local driving trends](https://www.waze.com/covid19)
<a name="about_waze_data"></a>
The driven kilometers/miles percent change data being shared comes from the Waze app and is aggregated and anonymized. These insights were generated using differential privacy to protect user privacy. No personally identifiable information, such as an individual’s location, contacts, or movement, is available through this data. 

These reports show the increase or decrease in driven kilometers/miles as a percent change compared to a baseline. The changes for each day are compared to a baseline value for that day of the week. 
* The baseline is the average value, for the corresponding day of the week, during the 2- week period February 11, 2020 to February 25, 2020. 
* The reports show trends over two weeks with the most recent data representing approximately 2-3 days ago. 

As with all samples, this may or may not represent the exact behavior of a wider population.

**Update interval:** ?

## Data explorer
<a name="data_explorer"></a>

### Google reports:
<a name="google_reports"></a>
[Raw CSV file](google_reports/Global_Mobility_Report.zip) (in ZIP archive). Direct link to the original CSV: https://www.gstatic.com/covid19/mobility/Global_Mobility_Report.csv

Data for the worldwide (only 1st level of subregions): [CSV](google_reports/mobility_report_countries.csv), [Excel](google_reports/mobility_report_countries.xlsx)

**Detailed reports:**

Data for the US: [CSV](google_reports/mobility_report_US.csv), [Excel](google_reports/mobility_report_US.xlsx)

Data for Brazil: [CSV](google_reports/mobility_report_brazil.csv), [Excel](google_reports/mobility_report_brazil.xlsx)

Data for Europe: [CSV](google_reports/mobility_report_europe.csv), [Excel](google_reports/mobility_report_europe.xlsx)

Data for Asia + Africa: [CSV](google_reports/mobility_report_asia_africa.csv), [Excel](google_reports/mobility_report_asia_africa.xlsx)

Data for North and South America + Oceania (Brazil and US excluded): [CSV](google_reports/mobility_report_america_oceania.csv), [Excel](google_reports/mobility_report_america_oceania.xlsx)

### Apple reports:
<a name="apple_reports"></a>
[Raw CSV file](apple_reports/applemobilitytrends.csv)

Data for the worldwide: [Google sheets](https://docs.google.com/spreadsheets/d/1KmTczsuu4G6Wki9EigjH-EH3xupirBG0ZKOK2qNAHJU/edit?usp=sharing), [CSV](apple_reports/apple_mobility_report.csv), [Excel](apple_reports/apple_mobility_report.xlsx)

Data for the US: [CSV](apple_reports/apple_mobility_report_US.csv), [Excel](apple_reports/apple_mobility_report_US.xlsx)

The following transformations have been made here:

* transformed dates from columns to rows
* transformed transportation types from rows to columns
* subtracted 100 from values (such as in Google Mobility Reports)

**Note: Data for May 11-12 is not available**

### Waze reports:
<a name="waze_reports"></a>
Raw CSV files: [Country-level](waze_reports/Waze_Country-Level_Data.csv), [City-level](waze_reports/Waze_City-Level_Data.csv)

Preprocessed report: [Google Sheets](https://docs.google.com/spreadsheets/d/1prxgtL1s8AvJDQb0hF2_g8rswwZElKQc2K79-FOmmt8/edit?usp=sharing), [CSV](waze_reports/waze_mobility.csv), [Excel](waze_reports/waze_mobility.xlsx)

### Summary reports:
<a name="summary_reports"></a>
These are merged Apple and Google reports.

Report by regions: [CSV](summary_reports/summary_report_regions.csv), [Excel](summary_reports/summary_report_regions.xlsx)

Report by countries: [Google Sheets](https://docs.google.com/spreadsheets/d/1d9t7xg-lUPEUArTsc_wMOGl1XfzpXmeWcALx7v58KcU), [CSV](summary_reports/summary_report_countries.csv), [Excel](summary_reports/summary_report_countries.xlsx)

Report for the US: [CSV](summary_reports/summary_report_US.csv), [Excel](summary_reports/summary_report_US.csv)

## How to run script
<a name="how_to_run_script"></a>
```bash
git clone https://github.com/ActiveConclusion/COVID19_mobility
pip install -r requirements.txt
python source.py
```
Also, available [Jupyter notebook](notebooks/Scraper%202.0.ipynb) mirror of this script

## Contributing
<a name="contributing"></a>
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. 

[Place to discuss use cases for this data](https://github.com/ActiveConclusion/COVID19_mobility/issues/4)

## Showcases
<a name="showcases"></a>
### Dashboards and visualizations based on these data
<a name="visualisations"></a>
1. [Dashboard for the US-1](https://public.tableau.com/profile/karl3594#!/vizhome/State-by-StateCOVID-19MobilityChanges/ChangesbyState)
2. [Dashboard for the US-2](https://public.tableau.com/profile/sky.quintin#!/vizhome/Mobilitydata/CommunityMobility)
3. [Dashboard for the world](https://public.tableau.com/profile/ryansoares#!/vizhome/COVID-19CommunityMobility/Dashboard1)
4. [Balefire COVID-19 USA Data Explorer](http://balefire.info/)
5. [Pandemic Traffic in Ireland](https://public.tableau.com/profile/docinsight#!/vizhome/COVIDtrafficinIrelandrepoint/MobilityDashboard) by David ó Cinnéide
6. [New South Wales COVID Tracking Dashboard](https://public.tableau.com/profile/damjan.vlastelica#!/vizhome/CovidNSWTracker/HomeDash?publish=yes) by Damjan Vlastelica
7. [Global COVID Vital Signs](https://eastnileuc.shinyapps.io/global_covidts/)
8. [Here can be your great dashboard/visualization]

### Articles and research publications
<a name="articles"></a>
1. [Is Your Community Doing Enough To Fight COVID-19?](https://towardsdatascience.com/is-your-community-doing-enough-to-fight-covid-19-aa745b424eb1) by [Molly Liebeskind](https://towardsdatascience.com/@molly.liebeskind)
2. [Project US Mobility and Fuel Demand Under COVID-19](https://covid19-mobility.com)
3. [COVID-19: Country progress tracker and forward projections](https://www.agility.asia/covid) 
4. [Here can be your great article/research publication]
