# SpaceX Falcon 9 First Stage Landing Prediction

## Project Overview
This project is part of the IBM Data Science Professional Certificate Capstone. The objective is to collect, clean, and analyze historical Falcon 9 launch data to predict whether the first stage will land successfully.

## Lab 1: Data Collection

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

## Lab 2: Data Wrangling (`labs-jupyter-spacex-Data wrangling.ipynb`)
- Performed Exploratory Data Analysis (EDA) on `dataset_part_1.csv` to determine the number of launches per site and the occurrence of each orbit type.
- Analyzed landing outcomes to categorize successful and unsuccessful landings.
- Created a binary classification target variable `Class` (1 for successful landing, 0 for unsuccessful).
- Calculated the overall landing success rate (approx. 66.7%).
- Exported the wrangled dataset for downstream EDA and machine learning as `dataset_part_2.csv`.

## Repository Files
- `dataset_part_1.csv`: Cleaned dataset from API data collection.
- `dataset_part_2.csv`: Wrangled dataset with the binary target variable `Class`.
- `spacex_web_scraped.csv`: Scraped dataset from Wikipedia.
- `jupyter-labs-spacex-data-collection-api.ipynb`: Jupyter Notebook for API data collection.
- `jupyter-labs-webscraping.ipynb`: Jupyter Notebook for web scraping.
- `labs-jupyter-spacex-Data wrangling.ipynb`: Jupyter Notebook for data wrangling.
