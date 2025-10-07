## Comparing Rainfall in Seattle and Hilo

>This code compares the rainfall in two different cities: Seattle, Washington and Hilo, Hawaii
---

## Project Overview

As part of the course, DATA 5100, I have been asked to investigate the relative rainfall in Seattle and a city of my choosing (Hilo, Hawaii) to determine which has more rainfall, ostensibly to win an argument with parental figures that it does **NOT** rain too much in Seattle. I will be using data collected by NOAA from the years: January 1, 2018 to December 31, 2022. Relative rainfall was assessed on these axes: 
- Maximum amount of rain in a given day
- Higher overall volume of rainfall in a given timeframe
- Higher average amount of rain in a given timeframe
- More days of rain across a given timeframe (2018-2022 in our case), and fewer days with 0 rain
Overwhelmingly, Hilo received more rain across each of these dimensions.



**Objective:** I am investigating whether it rains more in Seattle, WA or Hilo, Hawaii.

**Domain:** Natural Science

**Key Techniques:** Comparative Statistics, and Visualization. 

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** NOAA website: https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND.
- Steps used to download the FREE data:
  1. Set Observation Type to Daily Summaries
  2. Change the date range to 2018-01-01 to 2022-12-31
  3. Search for city of interest, in this case Seattle and Hilo and click search
  4. A map will be presented. Zoom in to pick one station of interest.
  5. Click Add to cart and go to cart. Do NOT be misled. The data is free
  6. Select the Output Format as Custom GHCN-Daily CSV. Check that the Data Range is 2018-01-01 to 2022-12-31. Click CONTINUE.
  7. Select Precipitation as a custom output for data. Continue
  8. Enter email. Receive data and download

- **Description:** The raw csv file will feature more columns than are of interest. The columns of interest are: STATION_NAME, DATE, and PRCP. STATION_NAME is the name of the station (usually city/airport name). DATE is formatted as a string where the year of the record (4 digits) followed by month (2 digits) and day (2 digits). These will later be standardized with Python dateTime library. PRCP = Precipitation (mm or inches as per user preference, I used inches)

---

## Analysis

For each notebook, simply run every cell in the order they are presented.

To clean the data first run the notebook titled: Seattle_Hilo_Weather

- the code will output a cleaned csv. Move the csv into  the data folder, else the analysis notebook will not know where to find the data
	
Then, to analyze the data run the notebook: Analysis_Seattle_Hilo_Weather

---

## Results

In order to assess rainfall in Seattle vs Hilo I asked these questions:
- What is the maximum amount of rain on any one given day? 
- Which city has the overall greater volume of rainfall in a given timeframe (monthly and yearly)? 
- Which city has the higher average amount of rain in a given timeframe (monthly, yearly)? 
- And which city has fewer days of 0 rain?

Overwhelmingly, Hilo was found to experience more rain than Seattle. The maximum amount of rained received in one day was 15in in Hilo compared to 2.6 in Seattle. Hilo received almost twice the amount of rain Seattle did every year, and the receives more rain monthly as well. Hilo rains 80% of the time compared to Seattle's barely over 50%. Hilo is the undisputed rain champion.


---

## Authors

- Ahrial Young - [@ayoung42](https://github.com/ayoung42)

---

## License
This project is licensed under the MIT License - see the LICENSE file for details.

---

## Acknowledgements

- libraries: pandas, numpy, maptplotlib, seaborns, scipy
- I followed data cleaning and exploration tutorials provided by Dr. Brian Fischer for his DATA 5100 FQ 2025 class. 
	[https://github.com/brian-fischer]
