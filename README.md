# SpaceX Falcon 9 First Stage Landing Prediction

## Project Overview
This project is part of the IBM Data Science Professional Certificate Capstone. The objective is to collect, clean, and analyze historical Falcon 9 launch data to predict whether the first stage will land successfully.

## Lab 1: Data Collection & Wrangling

### 1. SpaceX API Data Collection (`jupyter-labs-spacex-data-collection-api.ipynb`)
- Retrieved historical launch data via GET requests from the SpaceX API endpoint.
- Filtered datasets to isolate single-core, single-payload Falcon 9 missions up to November 13, 2020.
- Extracted granular booster specifications, payloads, launchpads, and core attributes using helper functions.
- Cleaned missing payload mass values using mean imputation and exported the dataset as `dataset_part_1.csv`.

### 2. Web Scraping Launch Records (`jupyter-labs-webscraping.ipynb`)
- Scraped historical Falcon 9 and Falcon Heavy launch records using `BeautifulSoup` from the Wikipedia snapshot.
- Extracted table headers (`<th>`) and iterated through launch table rows (`<tr>` and `<td>`).
- Parsed mission attributes including Flight Number, Launch Site, Version Booster, Orbit, Customer, and Landing Outcome.
- Exported the structured records to `spacex_web_scraped.csv`.

## Repository Files
- `dataset_part_1.csv`: Cleaned dataset from API data collection.
- `spacex_web_scraped.csv`: Scraped dataset from Wikipedia.
- `jupyter-labs-spacex-data-collection-api.ipynb`: Jupyter Notebook for API data collection.
- `jupyter-labs-webscraping.ipynb`: Jupyter Notebook for web scraping.
