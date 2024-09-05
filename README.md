# Web Scraping and Data Extraction Project

This project is a web-based application that scrapes information such as emails, phone numbers, and social media links from a given URL. It is built using Flask, BeautifulSoup, requests, and SQLite for storing scraped data. The application also includes an admin login system to view the scraped data.

## Features

- **Web Scraping**: Extracts emails, phone numbers, and social media links from websites.
- **Admin Login**: An admin login system allows authorized users to access the dashboard to view scraped data.
- **Data Storage**: Stores scraped data in a SQLite database.
- **Sublink Scraping**: Scrapes and stores information from linked subpages on the main website.
- **Automatic Data Storage**: Ensures the scraped data is saved in a structured format for easy retrieval.
- **Phone Number Validation**: Extracts and validates phone numbers using the `phonenumbers` library.

## Technologies

- **Flask**: Web framework for building the backend.
- **SQLite**: Database for storing scraped information and admin credentials.
- **BeautifulSoup**: HTML parsing library used for web scraping.
- **Requests**: For sending HTTP requests and retrieving web page content.
- **Phonenumbers**: For extracting and validating phone numbers.

  ### Prerequisites

Ensure you have Python and pip installed.

1. Clone the repository:

```bash
git clone https://github.com/prathiksha3/GITHUB.git
```
2.Install the required dependencies:

pip install -r requirements.txt

3.Set up the SQLite databases for scraped data and admin credentials:

The script already initializes these databases:
scraped_data.db: Stores scraped emails, phone numbers, and social media links.
admin_credentials.db: Stores admin credentials.

4.Update admin credentials in the database. You can change the default username and password in the following section of the code:

# Add admin credentials to the database
cursor.execute('INSERT OR REPLACE INTO admin_credentials (username, password) VALUES (?, ?)', ('admin_username', 'admin_password'))

# Usage

1.Run the Flask app:

python app.py

2.Access the application in your web browser at http://127.0.0.1:5000/.

3.Admin Login:

Enter the username and password configured in the admin_credentials.db database.
4.Scraping:

Input a URL to scrape for emails, phone numbers, social media links, and associated data from subpages.
5.View Data:

After logging in as an admin, you can view the scraped data on the dashboard.

# API Endpoints
/login: Admin login route.

/scrape: Scrape data from a user-provided URL.

/user: Admin dashboard for viewing all scraped data.
