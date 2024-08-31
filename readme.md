# PubMed Asynchronous Scraper

## Overview

`PubMed Asynchronous Scraper` is a Python script that asynchronously scrapes PubMed, an open-access database of scholarly research articles. The script extracts essential information such as titles, abstracts, author affiliations, keywords, and publication details. The collected data is then saved to a CSV file for further analysis.

## Features

- Asynchronous scraping using `aiohttp` and `asyncio`.
- Extracts titles, abstracts, affiliations, authors, journals, keywords, dates, and URLs.
- Outputs results in CSV format.
- Customizable scraping parameters, including date range and number of pages.
- Handles large-scale data extraction efficiently with asynchronous operations.

## Functions

- **`make_header`**: Generates HTTP request headers using a random user agent to avoid bans.
- **`get_num_pages`**: Determines the number of result pages returned by a keyword search.
- **`extract_by_article`**: Extracts data from a single PubMed article and formats it into a DataFrame.
- **`get_pmids`**: Retrieves PMIDs from a search results page and builds article URLs.
- **`build_article_urls`**: Asynchronously builds article URLs for each page of results for the provided keywords.
- **`get_article_data`**: Asynchronously scrapes data from each article URL and stores it in a DataFrame.

## Installation

### Clone the Repository


### Install Dependencies

Ensure you have Python 3.7+ installed. Then, install the required Python packages using:


### Requirements

Create a `requirements.txt` file with the following content:
beautifulsoup4 ,pandas ,requests ,aiohttp ,nest_asyncio
I have provided the dependency in **requirements.txt** install it

## Usage

1. **Prepare the Keywords File**: Create a `keywords.txt` file in the same directory with each line containing a keyword for scraping.
eg Machine Learning

2. **Run the Script**:

   Example command to run the script:

**python pubmed.py --pages 5 --start 2020 --stop 2023 --output research_articles.csv**


In this example:
- `--pages 5` specifies that 5 pages of results should be scraped for each keyword.
- `--start 2020` specifies the start year for the publication date range.
- `--stop 2023` specifies the end year for the publication date range.
- `--output research_articles.csv` specifies that the results should be saved to `research_articles.csv`.

3. **Check Output**: The results will be saved in `research_articles.csv` in the current directory.

## Project Structure

your-repo/
│
├── pubmed.py
├── requirements.txt
├── keywords.txt
└── README.md




