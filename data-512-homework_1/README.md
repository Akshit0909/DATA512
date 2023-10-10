## Project Goal

The primary aim of this endeavor is to monitor Wikipedia article viewership for a selection of Academy Award-winning film-related entries spanning from 2015 through 2023. The study aims to generate three distinct datasets: monthly traffic from mobile devices, monthly traffic from desktop computers, and cumulative monthly page views.

## Data Sources

- **Wikipedia Pageviews Data**: This project depends on the Wikimedia Foundation REST API for retrieving page view statistics of Wikipedia articles. The data covers the period from July 2015 up to the most recently completed month.

## Development Environment
*We encourage using [pyenv](https://github.com/pyenv/pyenv) to set up and configure your Python development environment.*
*This repo was built using Python 3.10*

## Data Processing and Analysis

The three major processes in the project are Data collection, data processing, and dataset development:

1. **Data Collection:** The project involves several key phases, with data acquisition being the first. This stage involves obtaining pageview counts for specific Wikipedia articles by utilizing the Pageviews API.

2. **Data Processing:** Subsequent to data acquisition, the retrieved information undergoes a processing step. During this phase, the data is organized into time series representations, effectively illustrating monthly pageview activity.

3. **Dataset Development:** The outcome of this project comprises three distinct datasets:
    - *Mobile Monthly Access:* This dataset encompasses pageviews from both mobile apps and mobile web, aggregated on a monthly basis.
    - *Desktop Monthly Access:* Specifically focusing on desktop pageviews, this dataset isolates this form of access.
    - *Monthly Cumulative:* This dataset consolidates the combined desktop and mobile traffic for each article on a monthly basis.

## Documentation

The project adheres to best practices for replication and documentation, ensuring transparency and ease of reproducibility:

- Jupyter Notebooks: Comprehensive explanations and instructions regarding data collection, processing, and analysis are provided within Jupyter Notebook(s).

- README File (this document): This file serves as a comprehensive overview of the project, delineating its goals, data sources, data processing methodologies, and standards for reproducibility.

- LICENSE File: Contained within this file is the project's MIT LICENSE, which ensures that the code can be freely utilized.

## License

This project is open-source and follows the MIT License. You are free to use and modify the code following the terms of the MIT License.

## API Documentation

- **Wikimedia Foundation REST API**: This project uses the Wikimedia Foundation REST API to access pageview data. For API documentation and terms of use, please visit: [Wikimedia Foundation REST API Documentation](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

## Known Issues

- A single article ("Victor/Victoria") yields a 404 API response, indicating that the URL for this article cannot be located.

- In the event of any difficulties with a specific API related to any of the articles, please reach out to the data owner specified in the source for assistance.

## Output Files

- The project generates three JSON files:
  - `academy_monthly_mobile_201507-202312.json`: Monthly mobile access data.
  - `academy_monthly_desktop_201507-202312.json`: Monthly desktop access data.
  - `academy_monthly_cumulative_201507-202312.json`: Monthly cumulative data.

Please refer to each file for detailed data on Wikipedia pageviews.

## Analysis Steps

1. Data Collection: Python code was employed for data retrieval from the Pageviews API.

2. Data Processing: The acquired data underwent processing to determine average pageviews, identify articles with both the highest and lowest pageview counts, and pinpoint articles with the least amount of available data.

3. Data Visualization: To present the research findings effectively, three graphical representations were generated:
    - Maximum and Minimum Average Page Requests
    - Top 10 Peak Page Views
    - Articles with the Least Data Coverage

4. Interpretation: To extract meaningful insights from the data, the analysis's findings were carefully interpreted.

## Reproducing the Analysis

To replicate this analysis, you can follow these steps:

1. Clone this repository onto your local machine.
2. Ensure that you have Python installed, along with the required libraries (pandas, matplotlib, json, requests, tqdm).
3. Execute the "data_acquisition.ipynb" file in Jupyter Notebook to generate the necessary JSON files.
4. Utilize the "data_visualization.ipynb" file in Jupyter Notebook to produce all the graphs, which will be stored in the parent directory.
5. Review the generated charts.

## Errors handled
The parameter safe='' was added to the urllib.parse.quote function so that it is able to handle cases like movie name 'Victor/Victoria' 
and does not give an error

## Output Files
The project generates three JSON files:
academy_monthly_mobile_201507-202312.json: Monthly mobile access data.
academy_monthly_desktop_201507-202312.json: Monthly desktop access data.
academy_monthly_cumulative_201507-202312.json: Monthly cumulative data.
Please refer to each file for detailed data on Wikipedia pageviews.

**Please Note:** For more comprehensive information and code implementation, please consult the provided Jupyter Notebook(s).

### Contributors
* [Akshit Miglani](https://www.linkedin.com/in/akshitmiglani/): akshit.miglani09@gmail.com | amiglani@uw.edu 