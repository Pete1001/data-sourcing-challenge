# data-sourcing-challenge
Module 6

# NASA CME and GST Data Retrieval and Analysis

This Jupyter Notebook retrieves Coronal Mass Ejection (CME) and Geomagnetic Storm (GST) data from NASA's DONKI API, processes the data, and analyzes the time differences between these events. The project involves data preparation, merging datasets, and exporting results to a CSV file for further use.

## Project Overview

The goal of this project is to:
1. **Retrieve data from NASA's DONKI API**: Request CME and GST data over a specific time period.
2. **Process and clean the data**: Expand linked events, extract activity IDs, and filter for relevant events.
3. **Merge datasets**: Combine CME and GST data on shared activity IDs.
4. **Analyze time differences**: Calculate the time delay between CME and GST events.
5. **Export the final results to CSV**: Save the processed data for future use.

## Features

- **Data Retrieval**: Uses NASA's API to fetch CME and GST events.
- **Data Processing**: Cleans and transforms the data, expanding linked events and extracting relevant fields.
- **Time Analysis**: Calculates the time difference between CME and GST events, showing how long it takes for a CME to cause a GST.
- **Visualization**: Displays a histogram of time differences between events.
- **CSV Export**: Saves the final merged dataset with important columns for future use.

## Requirements

- Python 3.x
- Required Python libraries: 
    - requests
    - pandas
    - matplotlib
    - dotenv (for loading NASA API key from an environment file)

## Installation

1. Clone the repository or download the notebook and necessary files.
2. Install required dependencies using pip:
    ```bash
    pip install -r requirements.txt
    ```
3. Create a `.env` file to store your NASA API key:
    ```
    NASA_API_KEY=your_nasa_api_key_here
    ```
4. Run the Jupyter Notebook.

## Usage

1. **CME Data Request**: Constructs a query URL to retrieve CME data using NASA's DONKI API.
2. **GST Data Request**: Retrieves GST data from NASA's API.
3. **Data Processing**:
    - Loops through the CME and GST data, expanding linked events.
    - Extracts activity IDs using custom functions.
    - Filters rows where events correspond to each other.
4. **Data Analysis**: Merges the CME and GST datasets and computes the time difference between events.
5. **Exporting Data**: The final merged dataset is exported to a CSV file without the index.

## Files

- `retrieve_data.ipynb`: Jupyter Notebook containing the full data retrieval, processing, and analysis code.
- `merged_data_export.csv`: CSV file containing the final processed and merged dataset.
- `.env`: A file storing your NASA API key (not included, must be created).

## Example

Below is a sample workflow of the project:

1. CME and GST data are retrieved via NASA's API.
2. Data is cleaned and processed to remove irrelevant rows.
3. Events are matched and time differences between CME and GST events are calculated.
4. A histogram is plotted to visualize the distribution of time differences.
5. The final dataset is exported to a CSV file.

## License

This project is licensed under the MIT License.
