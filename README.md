# RedBus-Project

Bus Details Scraper and Dashboard
Overview
This project consists of a data scraping script to collect bus details from multiple websites, a PostgreSQL database for storing the scraped data, and a Streamlit application to visualize and filter the bus data.

Features
Web Scraping: Automatically scrapes bus route information and bus details from specified websites.
Data Storage: Stores the scraped data into a PostgreSQL database.
Data Visualization: Provides an interactive dashboard using Streamlit to filter and display bus data.
Components
Data Scraping Script (scraper.py):

Scrapes bus route data and bus details from multiple websites.
Saves the scraped data into CSV files.
Loads the data into a PostgreSQL database.
Database Setup and Loading:

Creates a PostgreSQL database and table if they do not exist.
Inserts the scraped data into the PostgreSQL table.
Streamlit Application (app.py):

Connects to the PostgreSQL database.
Displays and filters the bus data in an interactive web application.
Installation
Prerequisites
Python 3.7 or later
PostgreSQL database
Required Python packages: psycopg2, pandas, sqlalchemy, selenium, streamlit
Steps to Set Up
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/bus-details-project.git
cd bus-details-project
Create and Activate a Virtual Environment

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Install Required Packages

bash
Copy code
pip install psycopg2 pandas sqlalchemy selenium streamlit
Set Up WebDriver

Download the appropriate WebDriver for your browser (e.g., ChromeDriver for Google Chrome).
Place the WebDriver executable in your system PATH or specify its location in the script.
Configure Database Connection

Open scraper.py and update the db_user, db_password, db_host, db_port, and db_name variables with your PostgreSQL connection details.
Run the Scraping Script

bash
Copy code
python scraper.py
This will scrape the bus data, save it to CSV files, and load it into the PostgreSQL database.

Run the Streamlit Application

bash
Copy code
streamlit run app.py
This will start the Streamlit server and open the application in your default web browser.

Usage
Scraping Data
The scraper.py script will scrape data from a list of predefined websites.
It will create route_data.csv and bus_data.csv files containing the scraped data.
The script will also create a PostgreSQL database and table, then load the data from the CSV files into the database.
Visualizing Data
Open the Streamlit app to visualize and filter bus data.
Use the sidebar to filter data by route name, bus type, star rating, and price.
The main area will display the filtered results based on the selected criteria.
Troubleshooting
Web Scraping Issues: Ensure that the websites' structure has not changed, as this may affect scraping. Adjust the XPath or class names in the script if necessary.
Database Connection Errors: Verify that PostgreSQL is running and the connection details are correct.
Streamlit Errors: Check for errors in the Streamlit logs and ensure that the database connection is correctly configured.
Contributing
Contributions are welcome! If you would like to contribute to this project:

Fork the repository.
Create a new branch for your feature or bug fix.
Make your changes and test them.
Submit a pull request with a clear description of the changes.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
Selenium: For automating web browser interaction.
Pandas: For data manipulation and analysis.
SQLAlchemy: For database interaction.
Streamlit: For creating interactive web applications.
