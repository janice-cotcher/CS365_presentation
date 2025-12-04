# CS 365 Final Project: Transit Regina Data Wrangling

## Dataset Information

- **Source:** City of Regina Open Data Portal
- **URL:** [Open Regina](https://open.regina.ca)
- **License:** Open Government License - Regina (allows educational use)
- **Raw Data:**
  - yqrStops.json (bus stops)
  - yqrRoutes.json (bus routes)
  - GTFS data (schedules and route details)

## Executable Files

- presentation.ipynb (Mercury slide presentation)
- transit_data.ipynb (Jupyter Notebook)

## Summary

This project cleans and transforms Regina transit data from geographic JSON files and General Transit Feed Specification(GTFS) schedule data. Key transformations include text standardization, type conversions, merging geographic and schedule data, deriving regional classifications, and calculating distances. The final dataset enables analysis of transit coverage and service patterns across Regina.

## How to Reproduce

1. Install dependencies: `pip install pandas plotly pyproj numpy`
2. Download and save the [Transit Stops Data JSON file](https://opengis.regina.ca/arcgis/rest/services/OpenData/TransitNetwork/MapServer/0/query?where=1=1&outFields=*&f=json) to `raw_data/` folder and rename it 'yqrStops.json'
3. Download and save the [Transit Routes Data JSON file](https://opengis.regina.ca/arcgis/rest/services/OpenData/TransitNetwork/MapServer/1/query?where=1=1&outFields=*&f=json) to `raw_data/` folder and rename it 'yqrRoutes.json'
4. Download the [Transit GTFS zip folder](https://openregina.ca/dataset/transit-network/resource/1509058a-409b-44b2-8e7e-e7b6056eff16) to 'raw_data'
5. Unzip 'google_transit.zip' and rename it 'gtfs_data'
6. Run notebook: `jupyter notebook transit_data.ipynb` or Execute all cells in order in VS Code

## Tool Versions

- Python: 3.14.0
- pandas: 2.3.3
- numpy: 2.3.5
- plotly: 6.5.0
- pyproj: 3.7.2

## AI Assistance Disclosure

No AI code generation tools were used. All code inserted by VS Code Extension: Data Wrangler is labelled. All other code was written manually by Janice Cotcher.
