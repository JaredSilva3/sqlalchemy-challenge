# SQLAlchemy Climate Analysis

## Project Overview

This project conducts a climate analysis of Hawaii using Python, SQLAlchemy ORM, Pandas, and Matplotlib. The analysis includes precipitation and station data retrieved from an SQLite database.

## Requirements

To successfully run the notebook and Flask API, the following Python packages are required:
- **flask**
- **numpy**
- **pandas**
- **sqlalchemy**

## Installation

Make sure that all required packages are installed before running the notebook or the Flask API. You can install them using conda:

```bash
conda install flask numpy pandas sqlalchemy

## How to Run the Flask API
1. Clone this repo to your local machine.
2. Open your terminal and create a new conda environment with the following command:
   `conda create -n climate_app python=3.12 numpy pandas flask sqlalchemy`
3. Activate the environment by running:
   `conda activate climate_app`
4. Navigate to the project directory.
5. Run the Flask app using:
   `python app.py`
6. Open your web browser and visit `http://127.0.0.1:5000/` to view the available routes.

## API Endpoints
- **Homepage**: `/`
  - Lists all available routes.
  
- **Precipitation Data**: `/api/v1.0/precipitation`
  - Returns the last 12 months of precipitation data in JSON format.
  
- **List of Stations**: `/api/v1.0/stations`
  - Returns a JSON list of stations.
  
- **Temperature Observations**: `/api/v1.0/tobs`
  - Returns temperature observations for the most active station.

- **Temperature Stats**:
  - For specific start date: `/api/v1.0/<start>`
  - For a range: `/api/v1.0/<start>/<end>`

## Database Structure
The database consists of the following tables:
- **measurement**: This table stores precipitation and temperature observation data.
- **station**: Contains information about weather stations.

The tables are connected using primary and foreign keys, allowing for relational queries between precipitation and station data.

## SQL Queries
The queries run in this project include:
- Retrieving the last 12 months of precipitation data.
- Listing all weather stations.
- Fetching temperature observations for the most active station.

## Challenges I Faced
One of the main challenges was managing the compatibility between different package versions, especially with NumPy and Pandas. After some troubleshooting, I ensured that all packages were correctly installed in the conda environment before running the Flask app.

## Final Thoughts
Overall, this project was a valuable exercise in setting up a Flask API, using SQLAlchemy for database interactions, and performing data analysis with Pandas. 