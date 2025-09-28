## Comparing Rainfall in Seattle and Hilo
> A brief description of what the project does and its purpose.
This code compares the rainfall in two different cities: Seattle, Washington and Hilo, Hawaii
---

## Project Overview

Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.

As part of the course, DATA 5100, I have been asked to investigate the relative rainfall in Seattle and a city of my choosing (Hilo, Hawaii) to determine which has more rainfall, ostensibly to win an argument with parental figures that it does **NOT** rain too much in Seattle. I will be using data collected by NOAA from the years: January 1, 2018 to December 31, 2022. Once I have completed the analysis I will discover:

- **Objective:** I am investigating whether it rains more in Seattle, WA or Hilo, Hawaii.
- **Domain:** Natural Science
- **Key Techniques:** Comparative Statistics, and Visualization. 

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

- **Description:** The raw csv file will feature more columns than are of interest. The columns of interest are: STATION_NAME, DATE, and PRCP. STATION_NAME is the name of the station (usually city/airport name). DATE is formatted as a string where the year of the record (4 digits) followed by month (2 digits) and day (2 digits). PRCP = Precipitation (mm or inches as per user preference, I used inches)
- **License:** (if applicable)

---

## Analysis

Describe the notebooks and/or scripts used to perform the analysis. Specify the order in which the code should be run to reproduce the results.

---

## Results

Include a short discussion of the findings and what they imply.

---

## Authors

- Ahrial Young - [@ayoung42](https://github.com/ayoung42)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used
- Tutorials or papers referenced
- Inspiration or collaborators
