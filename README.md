# Scraping and analysis squash ranking data from wikipedia

The primary aim of the project was to learn how to scrape data in python using BeautifulSoup, with secondary aim to see what patterns can be found in the scraped data.

## Directory structure

* `environment.yml` - environment file used to create the conda environment for this project
* `LICENSE` - contains license of this github repo
* `README.md` - this readme file
* `data`
  * `male_raw.csv` - raw data scraped from wikipedia for male players using `01-scrape.ipynb`
  * `female_raw.csv` - raw data scraped from wikipedia for female players using `01-scrape.ipynb`
  * `male_processed.csv` - processed data created from raw data and `02-process.ipynb`
  * `female_processed.csv` - processed data created from raw data and `02-process.ipynb`
* `notebooks`
  * `01-scrape.ipynb` - notebook used to scrape data from wikipedia. creates `male_raw.csv` and `female_raw.csv`
  * `02-process.ipynb` - notebook used to process data. creates `male_processsed.csv` and `female_processed.csv` from `male_raw.csv` and `female_raw.csv`
  * `03-analysis.ipynb` - notebook containing analysis of data. uses `male_processsed.csv` and `female_processed.csv`
  * `04-teachPCA.ipynb` - notebook used to help me teach PCA to somebody
