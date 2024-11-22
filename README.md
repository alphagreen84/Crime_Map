# **Visualize the criminals in your neigbourhood **

This code scrapes data from different sources and visualize persons that has been convicted in court.

![image](https://github.com/user-attachments/assets/0a22dcb4-b201-45c2-b258-ce461e506ea5)


[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)


---

## **Table of Contents**

1. [About the Project](#about-the-project)
2. [Getting Started](#getting-started)
3. [Overview](#overview)
4. [Usage](#usage)
5. [Features](#features)
6. [Technologies Used](#technologies-used)
7. [Installation](#installation)
8. [Output](#output)


---
## **About the Project**

The objective of this project is to grab data from a conviction database (get persons by city) and based on that data scrape further details about the persons location.
Finally visualize the persons location on a map.
- 🛒 Scrapes the krimfup.se and ratsit.se to gather location data using `Selenium` and `BeautifulSoup`.
- 🧠 Use Google Geocode API to make location name into lat/lon using `requests`.
- 📩 Plotting each locatoin on a Google Maps html file.


---

## **Features**
- Scrape name and location data from [Krimfup.se](https://www.krimfup.se/search).
- Use **Selenium** to fetch addresses from [Ratsit](https://www.ratsit.se).
- Geocode the addresses into latitude/longitude using the **Google Maps Geocoding API**.
- Save results in both JSON and CSV formats for further use.

---

## **Technologies Used**
- **Python**
- **Requests**: For sending HTTP requests to the websites.
- **BeautifulSoup**: For parsing and scraping HTML content.
- **Selenium**: For scraping dynamically loaded content from Ratsit.
- **Google Maps Geocoding API**: For geocoding addresses to latitude and longitude.
- **Pandas**: For data manipulation and storage.

---

## **Installation**

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

## **Output**
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

## **Files in the Project**
- main.py: Main script for scraping and geocoding.
- requirements.txt: Python dependencies for the project.
- locations.json: JSON file containing the final geocoded results.
- updated_dataframe_with_geocodes.csv: CSV file containing the tabular data.

## **Requirements**
- Python 3.7+
- Chrome Browser
- Google Maps Geocoding API key


## **Future Improvements**
- Add multi-threading for faster scraping and geocoding.
- Support for more dynamic websites.
- Scrape information like vehicles ownership.
- Make a heat map over congested areas.


