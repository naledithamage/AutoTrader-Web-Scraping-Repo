**AutoTrader Web Scraping Used Car Database**

**Overview**

This project involves web scraping data from the AutoTrader UK website to create a used car database. The data is visualized dynamically using a Bokeh Server application, allowing for easy exploration and analysis. The scraping process supports large-scale data collection with proxy settings for reliability.

**Features**
Scrapes used car listings from AutoTrader UK.
Builds a dataset that includes details such as make, model, price, year, mileage, fuel type, and more.
Visualizes the data interactively using a Bokeh Server.
Supports proxy settings for efficient large-scale scraping.
Dependencies

**To run this project, you’ll need the following Python libraries:**
requests
json
pandas
BeautifulSoup
numpy
bokeh
How to Run

**The process is divided into three simple steps:**

Step 1: Scrape Makes and Models
Run the script to collect all available makes and models:

python autoTraderScrapeMakesModels.py
Set output file and proxy settings in the script as needed.

Step 2: Scrape Used Car Listings
Run the script to retrieve car details based on the makes and models:

python autoTraderUsedCarScrape.py
Set input/output file names, proxy settings, and the number of pages to scrape in the script.

Step 3: Visualize Data with Bokeh
Use the Bokeh Server to create an interactive visualization:

Update the DATA_FILE variable in bokehServerAutoTrader.py with your dataset file.
Run the server:
bokeh serve --show bokehServerAutoTrader.py
The visualization will open in your browser.
Proxy Settings

For large-scale scraping, enable proxy settings to avoid being blocked by the website. Configure proxy details in the scripts for better reliability.

License

This project is licensed under the MIT License.

