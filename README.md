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
3. Download and install the Chrome WebDriver:
   Ensure the version matches your installed Chrome browser.

## Usage
1. Serve the google html map over http
    ```bash
    python -m http.server 8000

2. Run the script:
     ```bash
   python krimfup_ratsit_geocode.ipynb

3. Enter the name of the city when prompted.

4. View the generated files:
   - locations.json: Contains the scraped and geocoded data.
   - updated_dataframe_with_geocodes.csv: Contains a tabular format of the data.
   
6. Add your Google API key in the script:
   Replace "YOUR_GOOGLE_API_KEY" in the script with your actual API key.

## Output
   Example JSON (locations.json)
   ```bash
   [
    {
        "Name": "John Doe",
        "Address": "Example Street 12, Stockholm",
        "Lat": 59.329323,
        "Lon": 18.068581
    },
    {
        "Name": "Jane Roe",
        "Address": "Another Street 34 B, Göteborg",
        "Lat": 57.70887,
        "Lon": 11.97456
    }
]
 ```
Example CSV (updated_dataframe_with_geocodes.csv)
   ```bash
| Name      | City       | Address                       | Lat        | Lon        |
|-----------|------------|-------------------------------|------------|------------|
| John Doe  | Stockholm  | Example Street 12, Stockholm  | 59.329323  | 18.068581  |
| Jane Roe  | Göteborg   | Another Street 34 B, Göteborg | 57.708870  | 11.974560  |
```

## Files in the Project
- main.py: Main script for scraping and geocoding.
- requirements.txt: Python dependencies for the project.
- locations.json: JSON file containing the final geocoded results.
- updated_dataframe_with_geocodes.csv: CSV file containing the tabular data.

## Requirements
- Python 3.7+
- Chrome Browser
- Google Maps Geocoding API key


## Future Improvements
- Add multi-threading for faster scraping and geocoding.
- Support for more dynamic websites.
- Scrape information like vehicles ownership.
- Make a heat map over congested areas.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
