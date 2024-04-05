# Webscraping-using-Requests

This code extracts quotes and their authors from the HTML content of the webpage and writes them to a CSV file in a format where each line contains an author and their corresponding quote separated by a comma.

**Description:**
The script utilizes the requests library in Python to send HTTP GET requests to each page of the website containing quotes. It iterates through a range of page numbers (from 1 to 10) to scrape quotes from multiple pages.

**Key Components:**

1. **URL Generation:** The script dynamically generates the URL for each page using f-strings, incorporating the page number into the URL.
HTTP Request: It sends a GET request to each generated URL, retrieving the HTML content of the page.
2. **Parsing HTML:** After retrieving the HTML content, the script parses it line by line, searching for specific HTML elements that contain the quotes and their authors.
3. **Data Extraction:** It extracts the quotes and authors from the HTML content using string manipulation techniques to remove HTML tags and extract relevant text.
4. **Writing to CSV:** The extracted quotes and authors are then written to a CSV file named "quotes.csv". The file is opened in append mode ('a'), ensuring that new quotes are added to the existing file without overwriting previous entries. The encoding parameter is specified as 'utf-8-sig' to handle Unicode characters properly.

**Result:**
The result is a CSV file containing two columns: one for the author's name and another for their corresponding quote. Each row in the CSV file represents a single quote along with its author.
