**#AutoTrader Web Scraping Used Car Database**

**Overview:**
This repository contains code for a web scraping project that creates a comprehensive database of used cars from AutoTrader UK. The data is then dynamically visualized using a Bokeh Server application.

The scraped dataset can be used for various machine learning and data analysis projects, such as predicting used car prices. For an example of this, see my related repository: AutoTrader Used Car Price Prediction.

**Features:**
Scrapes car listings from AutoTrader UK based on make and model.
Dynamically visualizes the dataset with a Bokeh Server application.
Supports proxy settings for reliable and large-scale web scraping.
Achieved a 99.4% scraping success rate for several hundred thousand car listings.
Example Dataset
Here’s a sample of 10 random rows from the dataset:

Make	Model	Name	Price	Year	Miles	BHP	L	Trans	Fuel
Jeep	Grand Cherokee	Jeep Grand Cherokee 3.0 CRD V6 Overland 4x4 5dr	5989.0	2007.0	79800.0	215.0	3.0	Automatic	Diesel
Nissan	Qashqai	Nissan Qashqai 1.6 N-TEC 2WD 5dr	8500.0	2012.0	50000.0	113.0	1.6	Manual	Petrol
Audi	A4 Avant	Audi A4 AVANT TFSI SPORT 1.4 5dr	17200.0	2016.0	18379.0	148.0	1.4	Manual	Petrol
BMW	X5M	BMW X5 M 4.4 5dr	54991.0	2016.0	14808.0	575.0	4.4	Automatic	Petrol
Dacia	Sandero Stepway	Dacia Sandero Stepway 0.9 Ambiance 5dr	5995.0	2014.0	27000.0	90.0	0.9	Manual	Petrol
Dependencies

**This project requires the following Python libraries:**
requests
json
pandas
BeautifulSoup
numpy
bokeh

**How to Run the Project**

**The project is divided into three parts:**
Part One: Scraping Makes and Models
This step collects all available makes and models listed on AutoTrader.

**Run the script:**
python autoTraderScrapeMakesModels.py
User Configurations:

USING_PROXY: Enable/disable proxy settings.
PROXY_SETTINGS: Specify proxy settings if applicable.
OUTPUT_PKL_FILE: Name of the output file.
Part Two: Scraping Used Car Listings
Once you have the makes and models, this step retrieves detailed listings for the cars.

**Run the script:**
python autoTraderUsedCarScrape.py
User Configurations:

USING_PROXY: Enable/disable proxy settings.
PROXY_SETTINGS: Specify proxy settings.
PKL_READ_FILE: Input the file created in Part One.
PKL_OUT_FILE: Name of the output file.
MAX_PAGE_NUM: Number of search pages to scrape (each page contains 12 listings).
Part Three: Visualizing the Dataset
This step uses Bokeh Server to dynamically visualize the dataset.

Open the bokehServerAutoTrader.py file and set DATA_FILE to the output file from Part Two.
Run the Bokeh server from the command line:
bokeh serve --show bokehServerAutoTrader.py
A new tab will open in your browser with an interactive plot.
Troubleshooting

If you encounter issues with running the Bokeh Server, ensure your Anaconda PATH variables are correctly configured.

Proxy Settings for Reliable Scraping

Web scraping at scale often requires proxy settings to avoid being blocked by websites. This project supports the use of proxies for improved reliability and a higher success rate.

License

This project is licensed under the MIT License. See the LICENSE file for details.

Notes

The scraper can be run for extended periods to collect up to 500,000 car listings.
Feel free to experiment with different proxy configurations to optimize scraping performance.
