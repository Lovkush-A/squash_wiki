# Scrape and analyse squash ranking data from wikipedia

The primary aim of the project was to learn how to scrape data in python using BeautifulSoup, with secondary aim to see what patterns can be found in the scraped data. Due to time restrictions, I only analysed the male dataset.

The questions I looked at along with my answers were:

* Do any players standout?
  * Peter Nicol stands out for having such a lower average rating over a long period of time
  * Gregory Gaultier and Nick Matthews stand out for how many years they have been in the top 10 rankings
* Can we separate the absolute best players from the other top 10 players?
  * Turns out there is a simple criteria that does the job pretty well: what is the players single best ranking
* What subgroups of players can be identified?
  * Dimension reduction and clustering reveal three clear clusters: players with many years in the top 10/the best players, players who played in late 90s and early 2000s and players who are currently playing
  * For interactive Bokeh visuals of these clusters, open the `.html` files in the `plots` directory
  * For non-interactive plots, see below!

PCA visualisation:
![PCA visualisation of clusters](https://github.com/Lovkush-A/squash_wiki/blob/main/plots/pca.png)

tSNE visualisation:
![tsne visualisation of clusters](https://github.com/Lovkush-A/squash_wiki/blob/main/plots/tsne.png)

UMAP visualisation:
![UMAP visualisation of clusters](https://github.com/Lovkush-A/squash_wiki/blob/main/plots/umap.png)

## Blogpost

I wrote a [short summary blogpost on Medium](https://lovkush.medium.com/the-most-outstanding-male-squash-players-c5f2be2c8036) intended for a general audience.

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
* `plots` - directory containing bokeh plots (`.html` files) and seaborn plots (`.png` files)

## Missing values

There were no missing values in this dataset

## Installation

I used conda to manage my environments and the details of the environment are in the `environment.yml` file. To create a new package and install the packages used in this project, navigate to the route of the directory and run `conda env create -f environment.yml`

## Acknowledgements

All the work here is my own, though, I undoubtedly made use of various blogs and stackoverflow pages to get everything to work! I also thank the reviewer from the Udacity course for their feedback and suggestions.
