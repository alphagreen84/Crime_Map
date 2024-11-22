# Scraping and Geocoding Project

## Overview
This project automates the process of:
1. Scraping names and locations from a public website.
2. Fetching detailed addresses from **Ratsit** using the scraped names and locations.
3. Geocoding the addresses into latitude and longitude coordinates using the **Google Maps Geocoding API**.
4. Storing the final data in a JSON file (`locations.json`) and a CSV file (`updated_dataframe_with_geocodes.csv`).

---

## Features
- Scrape name and location data from [Krimfup.se](https://www.krimfup.se/search).
- Use **Selenium** to fetch addresses from [Ratsit](https://www.ratsit.se).
- Geocode the addresses into latitude/longitude using the **Google Maps Geocoding API**.
- Save results in both JSON and CSV formats for further use.

---

## Technologies Used
- **Python**
- **Requests**: For sending HTTP requests to the websites.
- **BeautifulSoup**: For parsing and scraping HTML content.
- **Selenium**: For scraping dynamically loaded content from Ratsit.
- **Google Maps Geocoding API**: For geocoding addresses to latitude and longitude.
- **Pandas**: For data manipulation and storage.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
