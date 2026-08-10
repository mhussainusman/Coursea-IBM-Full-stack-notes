# Course 7: Python for Data Science, AI & Development

## Module 5: APIs, Web Scraping, and Working with Files

### Key Concepts
- Understanding and using simple APIs in Python to interact with services and data.
- Working with REST APIs and HTTP methods to send and receive data over the internet.
- Extracting and parsing web data using web scraping techniques with Beautiful Soup.
- Handling different file formats such as CSV, JSON, XML, and Excel in Python using libraries like Pandas.

### Notes
This module covers how APIs serve as interfaces allowing software to communicate, with Python libraries facilitating API requests and data handling. REST APIs use HTTP methods like GET, POST, PUT, and DELETE to perform operations, often exchanging JSON data. Web scraping involves extracting data from HTML web pages using tools like Beautiful Soup, which parses HTML as a tree structure for easy navigation and data extraction. The module also explains working with various file formats, emphasizing how Python can read and write data in formats such as CSV, JSON, XML, and Excel, enabling efficient data manipulation and analysis.

### Code Examples
```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

# Example: Making a GET request to an API
response = requests.get('https://api.example.com/data')
data = response.json()

# Example: Parsing HTML with Beautiful Soup
html_doc = "<html><body><table><tr><td>Data</td></tr></table></body></html>"
soup = BeautifulSoup(html_doc, 'html.parser')
table = soup.find_all('table')

# Example: Reading CSV file with Pandas
df = pd.read_csv('data.csv')
print(df.head())
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| requests.get() | Sends a GET HTTP request to a specified URL |
| BeautifulSoup() | Parses HTML or XML documents for data extraction |
| find_all() | Finds all HTML elements matching criteria |
| pd.read_csv() | Reads CSV files into a Pandas DataFrame |
| head() | Displays the first few rows of a DataFrame |
| mean() | Calculates the mean of DataFrame columns |

### Glossary
- **API (Application Programming Interface)**: A set of functions and protocols allowing software to communicate.
- **REST API**: An API that uses HTTP requests to GET, POST, PUT, DELETE data.
- **HTTP Methods**: Commands like GET, POST, PUT, DELETE used to interact with web services.
- **JSON (JavaScript Object Notation)**: A lightweight data format used for data exchange.
- **Web Scraping**: Extracting data from websites by parsing HTML content.
- **Beautiful Soup**: A Python library for parsing HTML and XML documents.
- **Pandas**: A Python library for data manipulation and analysis.

### Summary
This module equips you with the skills to interact with APIs using Python, extract data from web pages through web scraping, and handle various file formats for data analysis. These capabilities are essential for collecting and processing data from diverse sources in data science and AI projects.